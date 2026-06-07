# Waste Management Route Compliance Suite

Waste collection route operations, container assets, landfill/recycling compliance, fleet, billing exceptions, and service quality.

**Buyer:** Waste haulers, recycling operators, municipalities

## Run

```bash
cd /Users/erolakarsu/external/projects/waste-management-route-compliance-suite
./start.sh
```

Open:

```text
http://127.0.0.1:5620
```

## Demo Logins

```text
admin@waste-management-route-compliance-suite.local / admin123
manager@waste-management-route-compliance-suite.local / manager123
analyst@waste-management-route-compliance-suite.local / analyst123
```

## Implemented Features

- Sidebar dashboard and module navigation
- Domain-specific workspaces: Routes, Containers, Fleet, Service Issues, Recycling Quality, Landfill Compliance, Billing Exceptions, Operations Analytics
- Seeded persistent data with 15 records per domain module
- Login, roles, local persistent JSON store
- Create, edit, delete records
- Document metadata upload workflow
- Tasks, notifications, audit logs
- CSV exports for every table
- AI Center with OpenRouter-ready endpoint and local fallback
- Reports and print-ready summaries
- Smoke test for health, login, CRUD, and export

## Test

```bash
npm test
```

For production, replace demo auth with an identity provider, replace local JSON with a database, add durable file storage, and validate AI workflows against your compliance requirements.


## Production-Style Feature Upgrade

Added across the full 20-app batch:

- API-enforced RBAC sessions for Admin, Manager, and Analyst roles
- Authorization checks for write, delete, export, AI, admin, and job endpoints
- Optimistic record versioning with conflict protection
- Server-side validation for required operational fields
- Rules-based risk scoring per record and module-level domain analysis
- Integrations, automations, approvals, tasks, notifications, documents, and audit logs
- Due-notification scheduled job endpoint plus hourly runtime scheduler
- Backup, restore, and reset endpoints
- Readiness endpoint with deployment checks
- Security response headers for API/static responses
- Expanded smoke tests covering RBAC, versioned CRUD, backup, jobs, domain analysis, and export
