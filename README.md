## Hi, I'm E. Black 👋

Cloud Architect focused on virtualization, enterprise backup, disaster recovery, and storage architectures.

---

### 🔧 Featured Project

#### [Veeam Designer](https://github.com/eblackrps/veeam_designer)

> Multi-site Veeam backup environment sizing and architecture tool — built for enterprise Veeam admins.

**v3.0.0 now available** — 10 major capability rounds:

| Module | What it does |
|---|---|
| VM Backup Sizing | Repository, proxy, SOBR, risk, 3-yr TCO |
| NAS / Unstructured | File proxy + cache repo sizing |
| Replication + CDP | Replica storage, CDP proxy/journal, WAN feasibility |
| WAN Accelerator | Appliance count, cache, BCJ window validation |
| VUL License Estimator | Workload count → community/standard/enterprise tier |
| LTO Tape Library | Cartridge, scratch pool, slots, drives, media cost |
| Veeam ONE + EM | Tiered server/RAM/DB, Enterprise Manager, VSPC |
| Compliance Gap Analysis | HIPAA · SOC 2 · GDPR · PCI DSS · DORA |
| HTML Design Report | Self-contained, print-ready downloadable report |
| REST API | `POST /api/design` · `GET /api/health` · `GET /api/profiles` |

**Install:**
```bash
pip install -e ".[web]"
uvicorn ui.main:app --reload
```

**Docker:**
```bash
docker pull emb079/veeam-designer
docker run -p 8000:8000 emb079/veeam-designer
```

[![GitHub release](https://img.shields.io/github/v/release/eblackrps/veeam_designer)](https://github.com/eblackrps/veeam_designer/releases)
[![Docker Pulls](https://img.shields.io/docker/pulls/emb079/veeam-designer)](https://hub.docker.com/r/emb079/veeam-designer)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/eblackrps/veeam_designer/blob/main/LICENSE)

---

### 🛠 Stack

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.100%2B-009688?logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-ready-2496ED?logo=docker&logoColor=white)
![pytest](https://img.shields.io/badge/tested%20with-pytest-0A9EDC?logo=pytest&logoColor=white)
