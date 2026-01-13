# Hotel Management Backend - API Reference

## Authentication & Authorization

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| POST | `/auth/register-hotel` | No | - | `{hotel_name, hotel_email, email, password}` | `{success, hotel_id}` | Register new hotel + owner account |
| POST | `/auth/login` | No | - | `{email, password}` | `{token, refresh_token, user: {email, role}}` | Login (Owner/Admin/Staff/Reception) |
| POST | `/auth/refresh` | No | - | `{refresh_token}` | `{token, refresh_token}` | Refresh JWT token |
| POST | `/auth/logout` | Yes | All | - | `{success}` | Logout & revoke tokens |

## Health & Status

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| GET | `/health/db` | No | - | - | `{status, timestamp}` | Database health check |

## AI Assistant & Chat

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| POST | `/api/ask` | No* | Guest | `{question, role, room_number, hotel_id}` | `{answer, sources, ticket_id?}` | AI concierge (RAG + Intent Detection) |
| POST | `/api/ask/refresh` | No | - | - | - | Refresh context (deprecated?) |

*Requires `hotel_id` in body

## Tickets (Service Requests)

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| GET | `/api/tickets` | No | - | `?hotel_id` | `{tickets: [...]}` | List all tickets |
| GET | `/api/tickets/filter` | No | - | `?hotel_id&status&role&priority` | `{tickets: [...]}` | Filter tickets |
| POST | `/api/tickets` | No | - | `{hotel_id, room_number, role, request, priority?}` | `{ticket}` | Create ticket |
| POST | `/api/tickets/assign` | No | - | `{ticket_id, staff_id, hotel_id}` | `{ticket}` | Assign ticket to staff |
| GET | `/api/tickets/room/:room_number` | No | - | `?hotel_id` | `{tickets: [...]}` | Get tickets by room |
| GET | `/api/tickets/floor/:floor` | No | - | `?hotel_id` | `{tickets: [...]}` | Get tickets by floor |
| GET | `/api/tickets/:ticket_id` | No | - | `?hotel_id` | `{ticket}` | Get single ticket |
| PATCH | `/api/tickets/:ticket_id/status` | No | - | `{hotel_id, status}` | `{ticket}` | Update ticket status |
| PATCH | `/api/tickets/:ticket_id/complete` | No | - | `{hotel_id, feedback?}` | `{ticket}` | Complete ticket |
| PATCH | `/api/tickets/:ticket_id/verify` | No | - | `{hotel_id, verified}` | `{ticket}` | Verify ticket resolution |
| PATCH | `/api/tickets/:ticket_id/assign` | Yes | RECEPTION | `{staff_id}` | `{ticket}` | Assign ticket (auth) |
| DELETE | `/api/tickets/:ticket_id` | No | - | `{hotel_id}` | `{success}` | Delete ticket |

## Inventory Management

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| GET | `/api/inventory` | No | - | `?hotel_id` | `{items: [...]}` | List all inventory items |
| GET | `/api/inventory/:id` | No | - | `?hotel_id` | `{item}` | Get single item |
| POST | `/api/inventory` | No | - | `{hotel_id, item_name, quantity, unit}` | `{success, item}` | Add new inventory item |
| PUT | `/api/inventory/:id` | No | - | `{hotel_id, item_name?, quantity?, unit?}` | `{success, item}` | Update inventory item |
| DELETE | `/api/inventory/:id` | No | - | `{hotel_id}` | `{success, message}` | Delete inventory item |

## Menu Management

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| GET | `/api/menu` | Yes | All | - | `{items: [...]}` | Get menu items |
| POST | `/api/menu` | Yes | OWNER, ADMIN | `{item_name, category, price, is_available}` | `{item}` | Add menu item |
| DELETE | `/api/menu/:menu_id` | Yes | OWNER, ADMIN | - | `{success}` | Remove menu item |
| PATCH | `/api/menu/:menu_id/toggle` | Yes | OWNER, STAFF, RECEPTION, ADMIN | - | `{item}` | Toggle item availability |

## Room Management

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| POST | `/api/rooms/checkin` | Yes | OWNER, RECEPTION | `{hotel_id, room_number, guest_name}` | `{session, guest_token}` | Check-in guest |
| POST | `/api/rooms/checkout` | Yes | OWNER, RECEPTION | `{hotel_id, room_number}` | `{success}` | Check-out guest |

## Staff Management

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| GET | `/api/staff/tickets` | No | - | `?staff_id&hotel_id` | `{tickets: [...]}` | Get staff's assigned tickets |
| POST | `/api/staff/register` | Yes | OWNER, ADMIN, DEVELOPER | `{email, password, role, hotel_id}` | `{staff_id}` | Register new staff member |

## Memory (Guest Preferences)

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| POST | `/api/memory` | No | - | `{hotel_id, room_number, role, content}` | `{success}` | Save room memory/preference |
| GET | `/api/memory` | No | - | `?hotel_id&room_number` | `{memories: [...]}` | Get room memories |

## Admin Dashboard

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| GET | `/api/admin/overview` | Yes | OWNER, ADMIN, DEVELOPER | - | `{stats}` | Dashboard overview stats |
| GET | `/api/admin/audit-logs` | Yes | OWNER, ADMIN, DEVELOPER | `?limit&offset` | `{logs: [...]}` | Audit trail logs |

## Orders (Food/Service)

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| POST | `/api/orders` | No | - | `{hotel_id, room_number, items, order_type}` | `{order}` | Create food/service order |

## Reception

| Method | Endpoint | Auth Required | Roles | Request Body | Response | Description |
|--------|----------|---------------|-------|--------------|----------|-------------|
| POST | `/api/reception` | No | - | `{email, password, hotel_id}` | `{reception_id}` | Register reception user |

---

## Common Request Headers

```
Content-Type: application/json
x-hotel-id: <uuid>  (optional, alternative to body/query param)
Authorization: Bearer <jwt_token>  (for protected routes)
```

## Common Response Codes

- `200` - Success
- `201` - Created
- `400` - Bad Request (missing params)
- `401` - Unauthorized (invalid credentials/token)
- `403` - Forbidden (insufficient permissions)
- `404` - Not Found
- `500` - Internal Server Error

## Multi-Tenancy

**All API endpoints require `hotel_id`** via:
- Request body: `{hotel_id: "uuid"}`
- Query param: `?hotel_id=uuid`
- Header: `x-hotel-id: uuid`

Row Level Security (RLS) enforces data isolation at database level.

## Auto-Features

### Inventory Deduction
When guests request items via `/api/ask`:
- AI extracts item + quantity
- Stock automatically deducted
- Low stock (<5) triggers high-priority alert to Reception

### Smart Ticket Management
- Duplicate detection (same request from same room)
- Auto-assignment to available staff
- SLA deadline calculation
- Feedback verification loop
