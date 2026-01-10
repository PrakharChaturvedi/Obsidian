
[[Sequence Diagram]]
#### 🧩 Hotel Manager Backend — API Structure Table

> **Base URL**: `http://localhost:3000`  
> **Auth**: JWT (Bearer)  
> **Hotel-scoped**: ✅ (JWT + RLS)

##### AUTH & SESSION APIs

| #   | Method | Endpoint               | Auth | Role   | Purpose                           |
| --- | ------ | ---------------------- | ---- | ------ | --------------------------------- |
| 1   | POST   | `/auth/register-hotel` | ❌    | Public | Create hotel + owner              |
| 2   | POST   | `/auth/login`          | ❌    | Public | Login (Owner / Staff / Reception) |
| 3   | POST   | `/auth/refresh`        | ❌    | Public | Refresh JWT using refresh token   |
| 4   | POST   | `/auth/logout`         | ✅    | Any    | Logout (revoke refresh token)     |
##### HOTEL / ADMIN APIs

| #   | Method | Endpoint                | Auth | Role          | Purpose                |
| --- | ------ | ----------------------- | ---- | ------------- | ---------------------- |
| 5   | GET    | `/api/admin/audit-logs` | ✅    | OWNER / ADMIN | Fetch hotel audit logs |
##### STAFF MANAGEMENT APIs

| #   | Method | Endpoint              | Auth | Role          | Purpose                       |
| --- | ------ | --------------------- | ---- | ------------- | ----------------------------- |
| 6   | POST   | `/api/staff/register` | ✅    | OWNER / ADMIN | Register hotel staff          |
| 7   | GET    | `/api/staff/tickets`  | ✅    | STAFF         | Get tickets assigned to staff |
##### RECEPTION APIs

| #   | Method | Endpoint                  | Auth | Role          | Purpose                 |
| --- | ------ | ------------------------- | ---- | ------------- | ----------------------- |
| 8   | POST   | `/api/reception/register` | ✅    | OWNER / ADMIN | Register reception user |
##### TICKET MANAGEMENT APIs

| #   | Method | Endpoint                         | Auth | Role        | Purpose                         |
| --- | ------ | -------------------------------- | ---- | ----------- | ------------------------------- |
| 9   | POST   | `/api/tickets`                   | ✅    | RECEPTION   | Create service ticket           |
| 10  | GET    | `/api/tickets`                   | ✅    | RECEPTION   | List all tickets (hotel-scoped) |
| 11  | GET    | `/api/tickets/:ticket_id`        | ✅    | Any (hotel) | Get ticket by ID                |
| 12  | GET    | `/api/tickets/room/:room_number` | ✅    | Any         | Tickets by room                 |
| 13  | GET    | `/api/tickets/floor/:floor`      | ✅    | Any         | Tickets by floor                |
| 14  | GET    | `/api/tickets/filter`            | ✅    | Any         | Filter tickets (floor/role)     |
| 15  | PATCH  | `/api/tickets/:ticket_id/status` | ✅    | STAFF       | Update ticket status            |
| 16  | PATCH  | `/api/tickets/:ticket_id/verify` | ✅    | RECEPTION   | Verify resolution               |
| 17  | DELETE | `/api/tickets/:ticket_id`        | ✅    | ADMIN       | Delete ticket                   |
##### ROOM MEMORY APIs

| #   | Method | Endpoint                   | Auth | Role      | Purpose                   |
| --- | ------ | -------------------------- | ---- | --------- | ------------------------- |
| 18  | POST   | `/api/memory`              | ✅    | RECEPTION | Add room memory           |
| 19  | GET    | `/api/memory/:room_number` | ✅    | STAFF     | Read room memory          |
| 20  | DELETE | `/api/memory/:room_number` | ✅    | SYSTEM    | Delete memory on checkout |
##### ROOM LIFECYCLE APIs (CHECK-IN / CHECK-OUT)

| #   | Method | Endpoint              | Auth | Role      | Purpose           |
| --- | ------ | --------------------- | ---- | --------- | ----------------- |
| 21  | POST   | `/api/rooms/checkin`  | ✅    | RECEPTION | Check-in guest    |
| 22  | POST   | `/api/rooms/checkout` | ✅    | RECEPTION | Checkout guest    |
| 23  | GET    | `/api/rooms/active`   | ✅    | RECEPTION | List active rooms |
##### CHAT / RAG APIs

| #   | Method | Endpoint        | Auth | Role              | Purpose             |
| --- | ------ | --------------- | ---- | ----------------- | ------------------- |
| 24  | POST   | `/api/ask`      | ✅    | Guest / Reception | Ask hotel assistant |
| 25  | POST   | `/api/chat/ask` | ✅    | Guest             | Guest-only chat     |
##### GUEST TOKEN / QR ACCESS

| #   | Method | Endpoint                  | Auth | Role   | Purpose              |
| --- | ------ | ------------------------- | ---- | ------ | -------------------- |
| 26  | POST   | `/api/rooms/token`        | ✅    | SYSTEM | Generate guest token |
| 27  | POST   | `/api/rooms/token/revoke` | ✅    | SYSTEM | Revoke guest access  |
##### SYSTEM / HEALTH

| #   | Method | Endpoint  | Auth | Role   | Purpose      |
| --- | ------ | --------- | ---- | ------ | ------------ |
| 28  | GET    | `/health` | ❌    | Public | Health check |
##### SECURITY & ENFORCEMENT (GLOBAL)

| Feature         | Status |
| --------------- | ------ |
| JWT Auth        | ✅      |
| Refresh Tokens  | ✅      |
| Rate Limiting   | ✅      |
| RBAC            | ✅      |
| Hotel Isolation | ✅      |
| Postgres RLS    | ✅      |
| Audit Logging   | ✅      |
#### HOW THIS ALL FITS TOGETHER (MENTAL MODEL)
- **Auth layer** → JWT + refresh tokens
- **RBAC middleware** → role-based access
- **Hotel isolation** → JWT + `app.hotel_id`
- **RLS** → DB enforces isolation even if code fails
- **Audit logs** → every critical action recorded
- **Room lifecycle** → check-in → memory → checkout → auto cleaning ticket


#### 🧾 RBAC MATRIX

| Action / API           | OWNER | ADMIN | RECEPTION | STAFF | GUEST | SYSTEM |
| ---------------------- | ----- | ----- | --------- | ----- | ----- | ------ |
| Register hotel         | ✅     | ❌     | ❌         | ❌     | ❌     | ❌      |
| Login                  | ✅     | ✅     | ✅         | ✅     | ❌     | ❌      |
| Refresh token          | ✅     | ✅     | ✅         | ✅     | ❌     | ❌      |
| Logout                 | ✅     | ✅     | ✅         | ✅     | ❌     | ❌      |
| View audit logs        | ✅     | ✅     | ❌         | ❌     | ❌     | ❌      |
| Register staff         | ✅     | ✅     | ❌         | ❌     | ❌     | ❌      |
| Register reception     | ✅     | ✅     | ❌         | ❌     | ❌     | ❌      |
| Check-in room          | ❌     | ❌     | ✅         | ❌     | ❌     | ❌      |
| Check-out room         | ❌     | ❌     | ✅         | ❌     | ❌     | ❌      |
| Create ticket          | ❌     | ❌     | ✅         | ❌     | ❌     | ❌      |
| View all tickets       | ❌     | ❌     | ✅         | ❌     | ❌     | ❌      |
| View assigned tickets  | ❌     | ❌     | ❌         | ✅     | ❌     | ❌      |
| Update ticket status   | ❌     | ❌     | ❌         | ✅     | ❌     | ❌      |
| Verify ticket          | ❌     | ❌     | ✅         | ❌     | ❌     | ❌      |
| Add room memory        | ❌     | ❌     | ✅         | ❌     | ❌     | ❌      |
| Read room memory       | ❌     | ❌     | ❌         | ✅     | ❌     | ❌      |
| Delete room memory     | ❌     | ❌     | ❌         | ❌     | ❌     | ✅      |
| Generate guest token   | ❌     | ❌     | ❌         | ❌     | ❌     | ✅      |
| Use guest token        | ❌     | ❌     | ❌         | ❌     | ✅     | ❌      |
| Create cleaning ticket | ❌     | ❌     | ❌         | ❌     | ❌     | ✅      |
##### 🔑Key RBAC Principles You Implemented (Correctly)
- **Least privilege** (staff cannot see hotel-wide data)
- **No guest write access**
- **Reception = orchestrator**
- **System role only used internally**
- **Owner/Admin only for sensitive ops**
This is **exactly how hotel PMS systems do it**.


