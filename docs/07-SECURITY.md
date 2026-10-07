# 07 - Security

## Security Documentation

### Authentication

Document:

- Identity provider
- Authentication method
- Token type
- Session behavior

### Authorization

Document:

- Roles
- Permissions
- RBAC
- Service identities

### Secrets

Never document actual secrets.

Bad:

```text
DATABASE_PASSWORD=MyRealPassword
```

Good:

```text
DATABASE_PASSWORD=<stored in secret manager>
```

### Security Checklist

- [ ] MFA
- [ ] Least privilege
- [ ] Secret management
- [ ] Encryption in transit
- [ ] Encryption at rest
- [ ] Logging
- [ ] Vulnerability scanning
- [ ] Dependency updates
- [ ] Backup protection

## Evidence Rule

If security control is not verified, mark it:

> ❓ Unknown — security configuration requires validation.
