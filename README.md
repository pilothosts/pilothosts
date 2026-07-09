<div align="center">

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://www.pilothosts.com/newlogo/pilothosts_logo_dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://www.pilothosts.com/newlogo/pilothosts_logo_light.svg">
    <img src="https://www.pilothosts.com/newlogo/pilothosts_logo_light.svg" alt="PilotHosts Logo" width="200">
  </picture>

### On-Prem Day-2 Operations Appliance for VMware/vSphere

PilotHosts connects to your vCenter through its native API and gives infrastructure teams operational visibility, governance, and automation across ESXi hosts, virtual machines, backups, and selected Kubernetes environments, all from a single self-contained OVA deployed inside your own infrastructure.

<p>
  <a href="https://www.pilothosts.com"><img alt="License" src="https://img.shields.io/badge/LICENSE-COMMERCIAL-3b82f6?style=for-the-badge&labelColor=0f172a"></a>
  <a href="https://www.pilothosts.com"><img alt="Website" src="https://img.shields.io/badge/WEBSITE-pilothosts.com-3b82f6?style=for-the-badge&labelColor=0f172a"></a>
  <a href="mailto:support@pilothosts.com"><img alt="Support" src="https://img.shields.io/badge/SUPPORT-EMAIL%20US-3b82f6?style=for-the-badge&labelColor=0f172a"></a>
</p>
<p>
  <img alt="Deployment" src="https://img.shields.io/badge/DEPLOYMENT-Self--Hosted%20OVA-1f2937?style=flat-square">
  <img alt="Agents" src="https://img.shields.io/badge/AGENTS-None%20Required-1f2937?style=flat-square">
  <img alt="Data residency" src="https://img.shields.io/badge/DATA-100%25%20On--Prem-1f2937?style=flat-square">
  <img alt="Connectivity" src="https://img.shields.io/badge/CONNECTIVITY-vCenter%20API%20Only-1f2937?style=flat-square">
  <img alt="Backup" src="https://img.shields.io/badge/BACKUP-Veeam%20Integrated-1f2937?style=flat-square">
</p>

**[Website](https://www.pilothosts.com) · [Documentation](https://www.pilothosts.com/docs/) · [Get a Trial](mailto:support@pilothosts.com) · [Report an Issue](https://github.com/pilothosts/pilothosts/issues)**

</div>

<br>

> This public repository hosts documentation, release notes, and issue tracking for PilotHosts. **The product source code is not published here.** PilotHosts is closed-source, commercially licensed, and is not affiliated with VMware, Broadcom, Veeam, Kubernetes, or the CNCF.

---

## Contents

- [What is PilotHosts?](#what-is-pilothosts)
- [At a Glance](#at-a-glance)
- [Features](#features)
- [Deployment](#deployment)
- [Requirements](#requirements)
- [Licensing](#licensing)
- [Support & Community](#support--community)

---

## What is PilotHosts?

PilotHosts is an on-premises VMware/vSphere day-2 operations appliance built for infrastructure teams who need visibility, governance, and operational control without sending data to the cloud.

It authenticates once against your **vCenter API** and, from there, gives you a unified view of ESXi hosts, virtual machines, backups, and selected Kubernetes environments. No direct ESXi connections, no agents installed anywhere in your environment, no infrastructure data ever leaves your network.

<div align="center">
<img src="https://www.pilothosts.com/assets/hybrid-architecture-diagram.svg" alt="PilotHosts hybrid infrastructure architecture diagram" width="760">
</div>

## At a Glance

| | |
|---|---|
| **Deployment model** | Single self-contained OVA appliance |
| **Data residency** | 100% on-premises: nothing sent to the cloud |
| **Agents required** | None |
| **Internet required** | No, after initial deployment |
| **Connectivity** | vCenter API only, ESXi hosts are never contacted directly |
| **Supported platforms** | VMware vCenter, Veeam Backup & Replication, selected Kubernetes & OpenShift |
| **Authentication** | Local, LDAP / Active Directory |

---

## Features

<details open>
<summary><strong>🖥️ Infrastructure Management</strong></summary>

- **Multi-vCenter Support**: manage multiple vCenter environments from a single pane of glass
- **ESXi Host Inventory**: real-time host status, CPU, memory, and connection state, pulled through the vCenter API
- **VM Inventory**: full VM listing with power state, owner, cluster, and datastore info
- **Tree View**: hierarchical vCenter → Datacenter → Cluster → Host → VM navigation
- **Topology View**: visual network topology of your infrastructure
</details>

<details>
<summary><strong>📊 Monitoring & Metrics</strong></summary>

- **CPU & RAM Analytics**: historical usage graphs per VM and per host
- **Storage Analyzer**: datastore capacity, growth trends, free space tracking
- **Resource Hogs**: identify top consumers across your environment
- **Oversized VMs**: detect over-provisioned VMs wasting resources
- **Anomaly Detection**: AI-powered detection of unusual CPU/RAM/storage patterns
- **Wallboard**: live dashboard for NOC/operations teams
</details>

<details>
<summary><strong>🛡️ Backup & Data Protection (Veeam)</strong></summary>

- **Veeam Integration**: connect and monitor Veeam Backup & Replication servers alongside your VMware inventory
- **Backup Job Monitoring**: job status, duration, processing rate, and bottleneck detection
- **Backup Chain Visualization**: restore point history and malware-scan status per VM
- **SLA Compliance Dashboard**: coverage tracking against your backup policies
- **Unprotected VM Detection**: surfaces VMs with no active backup job
</details>

<details>
<summary><strong>⚙️ Automation & Scheduling</strong></summary>

- **Task Scheduler**: schedule VM power operations, snapshots, and more
- **Ansible Integration**: run playbooks and job templates directly from the UI
- **Automated Snapshots**: policy-based snapshot scheduling with aging rules
- **Snapshot Aging Policies**: automatically clean up old snapshots
- **Autostart Management**: configure VM boot order for ESXi hosts
- **VM Lifecycle Management**: retirement workflows, zombie VM detection
</details>

<details>
<summary><strong>✅ Compliance & Governance</strong></summary>

- **Compliance Center**: scan your environment against best practice rules
- **Best Practice Scoring**: scored compliance dashboard with trend tracking
- **Weekly/Monthly Reports**: automated compliance report emails
- **Audit Logs**: full user action audit trail
- **Tools Compliance**: VMware Tools version tracking across all VMs
</details>

<details>
<summary><strong>📈 Capacity & Planning</strong></summary>

- **Capacity Planner**: model future growth and resource needs
- **Rightsizing Intelligence**: right-size VM CPU and memory allocations
- **Growth Curve**: storage and compute growth forecasting
- **Evacuation Planner**: plan host maintenance with workload migration analysis
- **Maintenance Readiness**: pre-maintenance checklist and impact assessment
</details>

<details>
<summary><strong>🔧 Operations</strong></summary>

- **Pilot Assistant**: AI-powered natural language interface for infrastructure queries
- **Infrastructure Doctor**: automated health checks and issue diagnosis
- **Governance Suite**: policy enforcement and governance reporting
- **SSL Certificate Manager**: track certificate expiry across your hosts
- **Bare Metal Management**: physical server inventory and management
- **VM Console**: browser-based VM console (WebMKS)
- **VM Create Wizard**: guided VM provisioning from templates
- **Deployments**: track VM and bare metal deployment workflows
</details>

<details>
<summary><strong>☸️ Kubernetes Visibility</strong></summary>

- **Cluster Management**: connect and monitor multiple Kubernetes clusters
- **Node Status**: regularly synced node health, resource usage, ready/not-ready state
- **Pod Monitoring**: pod status, crashloop detection, failed pod alerts
- **Namespace Overview**: resource usage and quota tracking per namespace
- **Workload Health**: deployment, daemonset, statefulset health monitoring
- **K8s Alerts**: notifications for node failures, pod crashes, quota warnings
</details>

<details>
<summary><strong>🔔 Notifications & Integrations</strong></summary>

- **Email Alerts**: SMTP-based alerts for CPU, RAM, storage, VM state changes
- **Webhook Support**: push events to Slack, Teams, or any HTTP endpoint
- **LDAP / Active Directory**: enterprise authentication support
- **Role-Based Access Control**: Superadmin, Admin, Operator, Viewer roles
</details>

---

## Deployment

PilotHosts is distributed as a self-contained **OVA appliance**.

1. Download the OVA from your license portal
2. Deploy to vSphere / ESXi (4 vCPU, 8 GB RAM, 60 GB disk recommended)
3. Power on: first boot configures SSL, keys, and services automatically
4. Open `https://<appliance-ip>` in your browser
5. Add your vCenter credentials and start managing

No internet connection required after deployment. All data stays on-premises.

---

## Requirements

| Size | Environment | vCPU | RAM | Disk |
|---|---|---|---|---|
| Medium | 1–5 vCenter / <1000 VMs | 4 | 16 GB | 250 GB |
| Large | 5+ vCenter / <10000 VMs | 8 | 32 GB | 250 GB |

| | Minimum | Recommended |
|---|---|---|
| vCenter | 7.0 (Tech Guidance only) | 8.0 |
| ESXi (managed through vCenter) | 7.0 | 8.0 |
| Veeam Backup & Replication | 12 | 12.x latest |

PilotHosts connects exclusively through the vCenter API: it never opens a direct connection to an ESXi host.

---

## Licensing

PilotHosts is commercial software. Licenses are available at [pilothosts.com](https://www.pilothosts.com).

A **trial license** is available: contact us at [support@pilothosts.com](mailto:support@pilothosts.com).

---

## Support & Community

| | |
|---|---|
| 📖 **Documentation** | [pilothosts.com/docs](https://www.pilothosts.com/docs/) |
| 🐛 **Bug Reports & Feature Requests** | [GitHub Issues](https://github.com/pilothosts/pilothosts/issues) |
| ✉️ **Email** | [support@pilothosts.com](mailto:support@pilothosts.com) |
| 🌐 **Website** | [www.pilothosts.com](https://www.pilothosts.com) |

---

<div align="center">

Made with care for VMware administrators everywhere.

**[www.pilothosts.com](https://www.pilothosts.com)**

</div>
