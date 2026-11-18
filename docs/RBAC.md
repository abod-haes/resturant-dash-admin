# RBAC & tenancy
| Capability | Primary Admin | Admin | Owner | Employee | Public |
|---|---|---|---|---|---|
| Create platform admins | Yes | No | No | No | No |
| Create restaurant/owner | Yes | Yes | No | No | No |
| Manage plan/subscription | Yes | Yes | Read own | No | No |
| Manage own branches/menu/tables/QR | Yes | Yes | Yes | No | No |
| Manage own employees/shifts | Yes | Yes | Yes | Own shift | No |
| Read call history | Yes | Yes | Own restaurant | Own branch permitted | No |
| Create call | No | No | No | No | Valid table session |
| View general menu | Yes | Yes | Yes | Yes | Yes |
Backend must enforce every row; UI hiding is not authorization. Admin operations audited. No cross-restaurant access.
