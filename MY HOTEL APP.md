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

