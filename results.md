### Task 1: Design Security Group Rules

| Rule | Type | Protocol | Port | Source | Purpose |
|------|------|----------|------|--------|---------|
| 1    | SSH  | TCP      | 22    | IP/32      | Admin access |
| 2    | HTTP    | TCP      | 80   | 0.0.0.0/0      | Web traffic |
| 3    | HTTPS    | TCP      | 443  | 0.0.0.0/0      | Secure web |
| 4    | Custom TCP | TCP | 8080  | 10.0.0.0/8 | Internal API |

### Task 5: Troubleshooting Exercise

| Symptom | Likely Cause | Solution |
|---------|--------------|----------|
| Can't SSH to instance | port 22 not allowed or wrong IP | add SSH rule with correct IP/32 |
| Website not loading | HTTP/HTTPS not allowed | allow ports 80 and/or 443 |
| API calls timing out | port 8080 blocked or wrong CIDR | allow TCP 8080 from 10.0.0.0/8 |