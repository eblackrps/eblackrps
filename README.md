## Eric Black · Cloud/DR Architect

Infrastructure engineer focused on backup architecture, disaster recovery automation, and resilience tooling. Building open-source tools for Veeam admins, platform engineers, and DR practitioners.

**Recovery Point** · [LinkedIn](https://linkedin.com/in/eb999)

---

### Projects

---

#### [veeam_designer](https://github.com/eblackrps/veeam_designer) · Python · v3.0.0

Multi-site Veeam backup environment sizing and architecture tool. Accepts a YAML project file and produces a full infrastructure blueprint — repo sizing, proxy count, SOBR layout, WAN/RPO feasibility, risk scoring, 3-year TCO, and more.

**10 sizing modules:**

| Module | What it sizes |
|---|---|
| VM Backup | Repository, proxy, SOBR, risk score, 3-yr TCO |
| NAS / Unstructured | File proxy + cache repo |
| Replication + CDP | Replica storage, CDP proxy/journal, WAN feasibility |
| WAN Accelerator | Appliance count, cache, BCJ window validation |
| VUL License Estimator | Workload count → community / standard / enterprise tier |
| LTO Tape Library | Cartridge, scratch pool, slots, drives, media cost |
| Veeam ONE + EM | Tiered server/RAM/DB, Enterprise Manager, VSPC |
| Compliance Gap Analysis | HIPAA · SOC 2 · GDPR · PCI DSS · DORA |
| HTML Design Report | Self-contained, print-ready downloadable report |
| REST API | `POST /api/design` · `GET /api/health` · `GET /api/profiles` |

```bash
docker pull emb079/veeam-designer
docker run -p 8000:8000 emb079/veeam-designer
```

[![Release](https://img.shields.io/github/v/release/eblackrps/veeam_designer)](https://github.com/eblackrps/veeam_designer/releases)
[![Docker Pulls](https://img.shields.io/docker/pulls/emb079/veeam-designer)](https://hub.docker.com/r/emb079/veeam-designer)
[![CI](https://github.com/eblackrps/veeam_designer/actions/workflows/ci.yml/badge.svg)](https://github.com/eblackrps/veeam_designer/actions/workflows/ci.yml)

---

#### [k8s-recovery-visualizer](https://github.com/eblackrps/k8s-recovery-visualizer) · Go · v1.0.0

Full Kubernetes cluster inventory and DR assessment tool. Scans a live cluster and produces a weighted DR readiness score across four domains, backup tool detection, restore simulation, and a prioritized remediation plan — all in a self-contained offline HTML report.

**What it measures:**

| Domain | Weight | Covers |
|---|---|---|
| Backup / Recovery | 30% | Tool presence, policy coverage, offsite config, RPO, restore simulation |
| Storage | 35% | PVC binding, StorageClass presence, hostPath, reclaim policies |
| Workload | 20% | StatefulSet persistence, deployment coverage |
| Config | 15% | CRD backup readiness, cert expiry, image registry risk, RBAC audit |

Maturity levels: **PLATINUM** (≥90) · **GOLD** (≥75) · **SILVER** (≥50) · **BRONZE** (<50)

Scoring profiles: `standard` · `enterprise` · `dev` · `airgap`

Auto-detects: Kasten K10, Velero, Longhorn, Rubrik, Trilio, Stash, CloudCasa

```bash
./scan --profile=enterprise --out ./out
./scan --ci --min-score=75 --out ./out
```

[![Release](https://img.shields.io/github/v/release/eblackrps/k8s-recovery-visualizer)](https://github.com/eblackrps/k8s-recovery-visualizer/releases)

---

#### [Hyper-v_cluster_scaffold](https://github.com/eblackrps/Hyper-v_cluster_scaffold) · PowerShell · v7.0.0

Enterprise-grade Hyper-V cluster deployment and compliance module for Windows Server 2025. Three execution modes — Audit, Enforce, Remediate — with a drift scoring engine (0–100), pre-change snapshot + rollback hook, HTML compliance reporting, and DSC resource scaffold.

```powershell
# Audit mode — read-only, generates compliance report
Invoke-HVClusterPlatform -ClusterName "ProdCluster" -Nodes @("NODE1","NODE2") -Mode Audit

# Enforce mode — snapshots, calculates drift, applies corrections
Invoke-HVClusterPlatform -ClusterName "ProdCluster" -Nodes @("NODE1","NODE2") -Mode Enforce
```

---

#### [ItsDeadJim](https://github.com/eblackrps/ItsDeadJim) · Chaos Simulation

Read-only chaos simulation tool that models backup failure blast radius before production does it for you. Maps dependency chains and quantifies the recovery impact of failures across your backup infrastructure.

---

#### [recovery-risk-translator](https://github.com/eblackrps/recovery-risk-translator) · Incident Narrative

Takes rough incident inputs and produces a clean, executive-safe post-incident DR narrative. Structured output for stakeholder communication after a recovery event.

---

### Stack

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?logo=powershell&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![Veeam](https://img.shields.io/badge/Veeam-00B336?logoColor=white)
