### RBAC Table

| Action              | OWNER | ADMIN | RECEPTION | STAFF |
| ------------------- | ----- | ----- | --------- | ----- |
| Register hotel      | ✅     | ❌     | ❌         | ❌     |
| Create staff        | ✅     | ✅     | ❌         | ❌     |
| Check-in guest      | ❌     | ❌     | ✅         | ❌     |
| Check-out guest     | ❌     | ❌     | ✅         | ❌     |
| Create ticket       | ❌     | ❌     | ✅         | ❌     |
| Update ticket       | ❌     | ❌     | ❌         | ✅     |
| Verify ticket       | ❌     | ❌     | ✅         | ❌     |
| View memory         | ❌     | ❌     | ❌         | ✅     |
| RAG query           | ❌     | ❌     | ✅         | ❌     |
| Logout all sessions | ✅     | ❌     | ❌         | ❌     |

### 🔐 AUTH & HOTEL SETUP

##### 1️⃣ Register Hotel + Owner
**POST** `http://localhost:3000/auth/register-hotel`
**Body :**
`{   "hotel_name": "Grand Palace Hotel",   "hotel_email": "admin@grandpalace.com",   "email": "owner@grandpalace.com",   "password": "StrongPassword@123" }`
✅ Expect:
`{   "success": true,   "hotel_id": "UUID" }`

##### 2️⃣ Login as OWNER
**POST** `http://localhost:3000/auth/login`
**Body**
`{   "email": "owner@grandpalace.com",   "password": "StrongPassword@123" }`
✅ Save in Postman environment:
`OWNER_JWT = token HOTEL_ID  = decoded.hotel_id`

---

### 🛎️ STAFF & RECEPTION

##### 3️⃣ Register Reception
**POST** `http://localhost:3000/api/reception/register`
**Headers**
`Authorization: Bearer {{OWNER_JWT}}`
**Body**
`{   "email": "reception@grandpalace.com",   "password": "Reception@123" }`

##### 4️⃣ Login Reception
**POST** `http://localhost:3000/auth/login`
**Body**
`{   "email": "reception@grandpalace.com",   "password": "Reception@123" }`
Save:
`RECEPTION_JWT`

##### 5️⃣ Register Staff
**POST** `http://localhost:3000/api/staff/register`
**Headers**
`Authorization: Bearer {{OWNER_JWT}}`
**Body**
`{   "name": "Ramesh",   "email": "ramesh.staff@grandpalace.com",   "password": "StaffPass@123",   "role": "housekeeping" }`

##### 6️⃣ Login Staff
**POST** `http://localhost:3000/auth/login`
**Body**
`{   "email": "ramesh.staff@grandpalace.com",   "password": "StaffPass@123" }`
Save:
`STAFF_JWT`


---
### 🏨 ROOM CHECK-IN / CHECK-OUT FLOW

##### 7️⃣ Room Check-In
**POST** `http://localhost:3000/api/rooms/checkin`
**Headers**
`Authorization: Bearer {{RECEPTION_JWT}}`
**Body**
`{   "room_number": 203,   "guest_name": "Mr. John Doe" }`
✅ Expect:
`{   "session": { "session_id": "UUID" },   "guest_token": "GUEST_JWT" }`
Save:
`GUEST_JWT`

---
## 8️⃣ Guest Uses Chat (Guest Token)

**POST** `http://localhost:3000/api/ask`
**Headers**
`Authorization: Bearer {{GUEST_JWT}}`
**Body**
`{   "question": "I need fresh towels",   "room_number": 203,   "role": "guest" }`
✅ This should **create a ticket automatically**

---
### 🎫 TICKETS

##### 9️⃣ List Tickets (Hotel-Scoped)
**GET** `http://localhost:3000/api/tickets`
**Headers**
`Authorization: Bearer {{RECEPTION_JWT}}`
Save:
`TICKET_ID`

##### 🔟 Staff Marks Ticket “On It”
**PATCH**  
`http://localhost:3000/api/tickets/{{TICKET_ID}}/status`
**Headers**
`Authorization: Bearer {{STAFF_JWT}}`
**Body**
`{ "status": "on_it" }`

##### 1️⃣1️⃣ Staff Completes Ticket
`{ "status": "done" }`

##### 1️⃣2️⃣ Reception Verifies
**PATCH**  
`/verify`

`{   "feedback": "Yes, everything is perfect" }`

---

# 🧠 ROOM MEMORY

---

## 1️⃣3️⃣ Add Room Memory

**POST** `http://localhost:3000/api/memory`

**Headers**

`Authorization: Bearer {{RECEPTION_JWT}}`

`{   "room_number": 203,   "message": "Guest is allergic to peanuts",   "role": "health" }`

---

## 1️⃣4️⃣ Get Room Memory (Staff)

**GET**  
`http://localhost:3000/api/memory/203`

**Headers**

`Authorization: Bearer {{STAFF_JWT}}`

---

# 🚪 ROOM CHECK-OUT (CRITICAL TEST)

---

## 1️⃣5️⃣ Check-Out Room

**POST** `http://localhost:3000/api/rooms/checkout`

`{   "room_number": 203 }`

✅ This MUST:

- ❌ Delete room memory
    
- ❌ Revoke guest token
    
- ✅ Create **cleaning ticket**
    

---

## 1️⃣6️⃣ Guest Token Should FAIL

Retry **Step 8** with same `GUEST_JWT`

❌ Expect:

`{ "error": "Invalid or expired token" }`

---

# 📋 AUDIT LOGS

---

## 1️⃣7️⃣ Fetch Audit Logs

**GET** `http://localhost:3000/api/admin/audit-logs`

**Headers**

`Authorization: Bearer {{OWNER_JWT}}`

✅ You should see:

- check-in
    
- ticket creation
    
- staff updates
    
- checkout
    
- memory deletion
    

---

# 🧨 SECURITY TESTS

---

## 1️⃣8️⃣ Cross-Hotel Access

Use JWT from another hotel → fetch ticket

❌ Expect:

`{ "error": "Not found" }`

---

## 1️⃣9️⃣ Rate-Limit Test

Spam login 6× in <1 hour

❌ Expect:

`{ "error": "Too many login attempts. Try again later." }`