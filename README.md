# Eric Black

**Infrastructure & Disaster Recovery Architect | Lead Solutions Architect & Operations Team Lead**

I design and operate disaster recovery and private-cloud environments, then build software to make the work easier to size, verify, troubleshoot, and recover. My background spans Veeam, VMware, Hyper-V, Nutanix AHV, Proxmox VE, Kubernetes/OpenShift, and multi-tenant recovery services.

The projects here are built around real operator problems: unclear sizing assumptions, missing recovery evidence, unsafe cleanup, and too many disconnected tools.

[**AnyStackArchitect**](https://www.anystackarchitect.com/) · [**Projects**](https://www.anystackarchitect.com/projects/) · [**LinkedIn**](https://www.linkedin.com/in/eb999/)

## Featured engineering projects

### Backup, recovery & infrastructure

- **[Veeam Designer](https://github.com/eblackrps/veeam_designer)** · **v5.0.0** · [Open the calculator](https://eblackrps.github.io/veeam_designer/)  
  Web-first Veeam architecture and sizing across virtualization platforms, repositories, retention, proxies, WAN, replication/CDP, and costs.

- **[Veeam XFS Backup-Copy Cleanup](https://github.com/eblackrps/xfs-file-cleanup)** · **v0.5.0** · [Download & operator guide](https://github.com/eblackrps/xfs-file-cleanup/releases/tag/v0.5.0)  
  Local Linux/XFS utility for reviewing expired Veeam backup-copy chains, with dry-run reports, metadata and immutability checks, and deletion auditing. Native v13 repository acceptance is still environment-specific; review the safety limits before a destructive run.

- **[K8 Visualizer](https://github.com/eblackrps/k8s-recovery-visualizer)** · **v1.10.5** · [Releases](https://github.com/eblackrps/k8s-recovery-visualizer/releases/latest)  
  Windows/Linux desktop toolkit for Kubernetes disaster recovery assessments, restore-readiness findings, offline bundle review, and comparison over time.

- **[GhostFleet](https://github.com/eblackrps/ghostfleet)**  
  Synthetic VM fleet and workload-data generator for repeatable backup, storage efficiency, deduplication, compression, and change-rate testing across virtualization platforms.

### Applications & operations tooling

- **[DC Coms](https://github.com/eblackrps/dc-coms)** · **v1.0.1 GA** · [Release](https://github.com/eblackrps/dc-coms/releases/tag/v1.0.1)  
  Self-hosted Matrix communications with encrypted chat, operator services, backup/recovery procedures, and repeatable RHEL-family deployment.

- **[MCP Home](https://github.com/eblackrps/mcp-home)**  
  Read-only MCP operations tools for Windows homelabs: Docker, Plex, service health, storage, files, and repository visibility.

- **[BlackFlag Audio](https://blackflagaudio.com/)** · **Private beta** · [Public website source](https://github.com/eblackrps/blackflagaudio.com)  
  Local-first Windows music library and player focused on controlled scans, duplicate review, and preview-first metadata changes. The application source is private.

- **[DR DOOM](https://github.com/eblackrps/dr-doom)**  
  A DOOM-inspired browser game built around disaster recovery concepts and an RTO clock. Sometimes the lab needs a sense of humor.

## What I work on

**Recovery:** DRaaS, backup and recovery architecture, cyber recovery, immutable storage, recovery testing, and operational runbooks.

**Platforms:** VMware vSphere, Microsoft Hyper-V, Nutanix AHV, Proxmox VE, Kubernetes, OpenShift, and private/hybrid cloud.

**Development:** Python, Go, PowerShell, TypeScript, React, automation, and Model Context Protocol (MCP) integrations.

## Writing & field guides

At [**AnyStackArchitect**](https://www.anystackarchitect.com/), I write about infrastructure design, disaster recovery, Veeam, virtualization, Kubernetes, migrations, and the operational details that turn up after a design leaves the whiteboard. Technical articles and field guides are free to read.

## How I build

- Start with a real operational problem and make assumptions visible.
- Prefer read-only inspection, dry runs, and explicit confirmation before destructive changes.
- Test recovery behavior and failure paths, not just the happy path.
- Ship usable documentation and reproducible checks alongside the software.

Public work here is my own engineering and experimentation. The complete repository list includes smaller tools and supporting projects.
