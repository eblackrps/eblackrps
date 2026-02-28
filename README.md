# Eric Black

Cloud & Disaster Recovery Architect. I build tooling around **tested recovery**, not just backup presence.

> *Backups are not strategy. Tested recovery is strategy.*  
> *Automation should reduce risk, not just reduce clicks.*

---

## Focus

- DR architecture validation and scoring
- Backup coverage analysis and gap detection
- Recovery simulation and failure blast radius modeling
- Infrastructure automation for service providers
- Kubernetes data protection workflows

---

## Projects

### [k8s-recovery-visualizer](https://github.com/eblackrps/k8s-recovery-visualizer)

Go CLI that scans a live Kubernetes cluster and produces a weighted DR readiness score across four domains. Collects 18+ resource types, auto-detects 7 backup tools, and generates a fully self-contained HTML report with prioritized remediation steps, historical trend tracking, and scan-to-scan diff.

```
scan --target=vm --csv --namespace=prod,staging --compare=./last-scan.json
```

| Domain | Weight | What It Measures |
|---|---|---|
| Storage | 35% | PVC binding, storageClass, hostPath, reclaim policies |
| Workload | 20% | StatefulSet persistence, deployment coverage |
| Config | 15% | CRD backup readiness, certificate expiry, image registry risk |
| Backup/Recovery | 30% | Tool presence, policy coverage, Helm values, public images |

**Maturity tiers:** PLATINUM · GOLD · SILVER · BRONZE  
**Output:** JSON, enriched JSON, Markdown, self-contained HTML, CSV

---

### [ItsDeadJim](https://github.com/eblackrps/ItsDeadJim)

Read-only chaos simulation tool that models backup failure blast radius before production does it for you. Maps recovery dependencies and sequences, surfaces risk before a DR event occurs.

---

### [recovery-risk-translator](https://github.com/eblackrps/recovery-risk-translator)

Takes rough incident inputs and produces a clean, executive-safe post-incident DR narrative. Bridges the gap between technical recovery timelines and business communication requirements.

---

### [veeam_designer](https://github.com/eblackrps/veeam_designer)

Environment planning and architecture sizing tooling for Veeam deployments.

---

### [Hyper-v_cluster_scaffold](https://github.com/eblackrps/Hyper-v_cluster_scaffold)

PowerShell-driven framework for Hyper-V cluster deployment in lab and production testing environments.

---

## Stack

Go · PowerShell · Kubernetes · Veeam · VMware · Hyper-V
