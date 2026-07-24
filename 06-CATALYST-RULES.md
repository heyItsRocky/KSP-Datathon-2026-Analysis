# 06 — Catalyst Deployment Rules

Critical constraints for Zoho Catalyst deployment.

---

## Mandatory Rules

1. **Deploy on Catalyst** — All submissions must run on Catalyst
2. **Use native services** — Data Store, Functions, API Gateway, Slate
3. **No external DB** — PostgreSQL, MySQL, SQLite not allowed
4. **No external auth** — Must use Catalyst Authentication
5. **Synthetic data only** — No real crime data
6. **Public GitHub repo** — Required for submission

## What's Allowed

| Service | Use Case |
|---------|----------|
| Catalyst Data Store | 26 tables (ZCQL) |
| Catalyst Functions | Python/Node.js backend |
| Catalyst API Gateway | Routing, CORS, auth |
| Catalyst Slate | Static frontend hosting |
| Catalyst Authentication | Login/session |
| Catalyst Cron | Scheduled tasks |
| Catalyst SmartBrowz | Web scraping |
| Catalyst Stratus | File storage |

## What's NOT Allowed

- External databases (PostgreSQL, MySQL, MongoDB)
- External auth (Auth0, Firebase)
- Docker containers in production
- Custom servers
- Unapproved external APIs

## Submission Checklist

- [ ] Public GitHub repo
- [ ] Frontend deployed on Slate
- [ ] Backend functions deployed
- [ ] Data Store with 26 tables
- [ ] Seed data loaded
- [ ] Prototype brief
- [ ] Demo video
- [ ] Submission template

---

*Generated: 2026-07-24*