# 06 - Network

## Network Documentation Template

### Connectivity

```text
Internet
   |
   v
WAF / Load Balancer
   |
   v
Application
   |
   v
Private Database
```

### Network Inventory

| Resource | Network | Subnet | Exposure | Status |
|---|---|---|---|---|
| API | VNet-01 | AppSubnet | Private | ✅ |
| DB | VNet-01 | DataSubnet | Private | ✅ |
| Admin endpoint | Unknown | Unknown | Unknown | ❓ |

### Questions

- Which resources are public?
- Which ports are open?
- Are NSGs/firewalls configured?
- Is private connectivity used?
- How is DNS resolved?
- Is outbound traffic restricted?
