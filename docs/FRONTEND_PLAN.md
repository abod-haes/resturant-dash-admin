# Super Admin Web — React + Vite
## Scope
Admin accounts, restaurants/owners, branch visibility, plans and manual subscriptions, contact channels, global audit, platform monitoring. No self-service checkout.

## Architecture
`src/app` providers/router; `src/features/{auth,restaurants,admins,plans,subscriptions,contact-methods,audit}`; `src/shared/{ui,api,types,lib,config}`; `src/mocks/{handlers,scenarios}`.
TanStack Query for server state; typed HTTP adapter; Zod schema validation; accessible RTL design system with reusable DataTable, FormField, Modal, Toast, EmptyState, Skeleton and ConfirmDialog. Never couple UI to fixture structure.

## Sequence
1. Design tokens and app shell, auth, protected routes.
2. Typed API layer, mock adapters/MSW and scenario switcher (development only).
3. Restaurant CRUD, owner credentials, branch details.
4. Plans, limits, manual subscription lifecycle and contact methods.
5. Admin management, audit log, analytics/monitoring.
6. Contract tests, accessibility, responsive, E2E; switch to live API by config.

## Quality gates
No hardcoded roles, no direct fetch in components, every table paginated on server, error/empty/loading states, audit-sensitive actions require confirmation, no secrets in browser storage, tests for tenant isolation and expired subscription.
