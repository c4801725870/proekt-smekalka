# Deployment Context — Smekalka

**Purpose:** Track deployment procedures, environments, and release status.
**Last updated:** 2026-09-20

---

## Environments

| Environment | URL/Host | Purpose | Deploy Method |
|-------------|----------|---------|---------------|
| Local | localhost | Development | Manual |
| Staging | TBD | Pre-production testing | TBD |
| Production | TBD | Live system | TBD |

---

## Deployment Checklist Template

```markdown
## Deploy [VERSION] to [ENVIRONMENT] — [YYYY-MM-DD]

### Pre-deploy
- [ ] All tests passing
- [ ] Code review complete
- [ ] Changelog updated
- [ ] Database migrations ready
- [ ] Environment variables updated
- [ ] Dependencies updated

### Deploy
- [ ] Stop services
- [ ] Backup database
- [ ] Pull new code
- [ ] Run migrations
- [ ] Install dependencies
- [ ] Start services
- [ ] Verify health check

### Post-deploy
- [ ] Smoke test passed
- [ ] Monitoring shows no errors
- [ ] User verification
- [ ] Update status page
```

---

## Rollback Procedure

```markdown
## Rollback to [PREVIOUS_VERSION]

1. Stop services
2. Restore database from backup
3. Checkout previous version
4. Run any reverse migrations
5. Start services
6. Verify health check
7. Notify stakeholders
```

---

## Release History

| Version | Date | Environment | Status | Notes |
|---------|------|-------------|--------|-------|
| — | — | — | — | No deployments yet |

---

## Current Deploy Status

| Environment | Version | Last Deploy | Status |
|-------------|---------|-------------|--------|
| Local | — | — | Not deployed |
| Staging | — | — | Not deployed |
| Production | — | — | Not deployed |
