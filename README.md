<div align="center">

<img src="https://www.pilothosts.com/newlogo/pilothosts_logo_dark.svg" alt="PilotHosts Logo" width="200" />

PilotHosts is a commercial on-prem appliance for VMware/vSphere day-2 operations.

This repository is used for public documentation, release notes and issue tracking.
The source code is not published here.
PilotHosts is not affiliated with VMware or Broadcom.

**Enterprise VMware & Kubernetes Management Appliance**

Manage, monitor, and automate your vCenter, ESXi hosts, virtual machines, and Kubernetes clusters — deployed as a self-contained OVA inside your own infrastructure.

[![License](https://img.shields.io/badge/license-Commercial-blue.svg)](https://www.pilothosts.com)
[![Website](https://img.shields.io/badge/website-pilothosts.com-blue)](https://www.pilothosts.com)
[![Support](https://img.shields.io/badge/support-support%40pilothosts.com-blue)](mailto:support@pilothosts.com)

</div>

---

## What is PilotHosts?

PilotHosts is an **on-premises VMware & Kubernetes management appliance** that gives IT teams full visibility and control over their vCenter/ESXi environments and Kubernetes clusters — without sending data to the cloud.

Deploy the OVA once. No agents. No SaaS subscriptions. No data leaving your network.

---

## Features

### Infrastructure Management
- **Multi-vCenter support** — manage multiple vCenter environments from a single pane of glass
- **ESXi Host Inventory** — real-time host status, CPU, memory, connection state
- **VM Inventory** — full VM listing with power state, owner, cluster, datastore info
- **Tree View** — hierarchical vCenter → Datacenter → Cluster → Host → VM navigation
- **Topology View** — visual network topology of your infrastructure

### Monitoring & Metrics
- **CPU & RAM Analytics** — historical usage graphs per VM and per host
- **Storage Analyzer** — datastore capacity, growth trends, free space tracking
- **Resource Hogs** — identify top consumers across your environment
- **Oversized VMs** — detect over-provisioned VMs wasting resources
- **Anomaly Detection** — AI-powered detection of unusual CPU/RAM/storage patterns
- **Wallboard** — live dashboard for NOC/operations teams

### Automation & Scheduling
- **Task Scheduler** — schedule VM power operations, snapshots, and more
- **Ansible Integration** — run playbooks and job templates directly from the UI
- **Automated Snapshots** — policy-based snapshot scheduling with aging rules
- **Snapshot Aging Policies** — automatically clean up old snapshots
- **Autostart Management** — configure VM boot order for ESXi hosts
- **VM Lifecycle Management** — retirement workflows, zombie VM detection

### Compliance & Governance
- **Compliance Center** — scan your environment against best practice rules
- **Best Practice Scoring** — scored compliance dashboard with trend tracking
- **Weekly/Monthly Reports** — automated compliance report emails
- **Audit Logs** — full user action audit trail
- **Tools Compliance** — VMware Tools version tracking across all VMs

### Capacity & Planning
- **Capacity Planner** — model future growth and resource needs
- **Rightsizing Intelligence** — right-size VM CPU and memory allocations
- **Growth Curve** — storage and compute growth forecasting
- **Evacuation Planner** — plan host maintenance with workload migration analysis
- **Maintenance Readiness** — pre-maintenance checklist and impact assessment

### Operations
- **Pilot Assistant** — AI-powered natural language interface for infrastructure queries
- **Infrastructure Doctor** — automated health checks and issue diagnosis
- **Governance Suite** — policy enforcement and governance reporting
- **SSL Certificate Manager** — track certificate expiry across your hosts
- **Bare Metal Management** — physical server inventory and management
- **VM Console** — browser-based VM console (WebMKS)
- **VM Create Wizard** — guided VM provisioning from templates
- **Deployments** — track VM and bare metal deployment workflows

### Kubernetes Visibility
- **Cluster Management** — connect and monitor multiple Kubernetes clusters
- **Node Status** — real-time node health, resource usage, ready/not-ready state
- **Pod Monitoring** — pod status, crashloop detection, failed pod alerts
- **Namespace Overview** — resource usage and quota tracking per namespace
- **Workload Health** — deployment, daemonset, statefulset health monitoring
- **K8s Alerts** — notifications for node failures, pod crashes, quota warnings

### Notifications & Integrations
- **Email Alerts** — SMTP-based alerts for CPU, RAM, storage, VM state changes
- **Webhook Support** — push events to Slack, Teams, or any HTTP endpoint
- **LDAP / Active Directory** — enterprise authentication support
- **Role-Based Access Control** — Superadmin, Admin, Operator, Viewer roles

---

## Deployment

PilotHosts is distributed as a self-contained **OVA appliance**.

```
1. Download the OVA from your license portal
2. Deploy to vSphere / ESXi (4 vCPU, 8 GB RAM, 60 GB disk recommended)
3. Power on — first boot configures SSL, keys, and services automatically
4. Open https://<appliance-ip> in your browser
5. Add your vCenter credentials and start managing
```

No internet connection required after deployment. All data stays on-premises.

---

## Tech Stack

| Component | Technology |
|---|---|
| Backend | Python / Flask / Gunicorn |
| Database | PostgreSQL + TimescaleDB |
| Cache | Redis |
| Web Server | Nginx |
| Deployment | OVA (VMware compatible) |

---

## Requirements

| Size | Environment | vCPU | RAM | Disk |
|---|---|---|---|---|
| Medium | 1–5 vCenter / <1000 VMs | 4 | 16 GB | 250 GB |
| Large | 5+ vCenter / <10000 VMs | 8 | 32 GB | 250 GB |

| | Minimum | Recommended |
|---|---|---|
| vCenter | 7.0 | 7.0 / 8.0 |

---

## Licensing

PilotHosts is commercial software. Licenses are available at [pilothosts.com](https://www.pilothosts.com).

A **trial license** is available — contact us at [support@pilothosts.com](mailto:support@pilothosts.com).

---

## Support & Community

- **Documentation:** [docs.pilothosts.com](https://docs.pilothosts.com)
- **Bug Reports & Feature Requests:** [GitHub Issues](https://github.com/pilothosts/pilothosts/issues)
- **Email:** [support@pilothosts.com](mailto:support@pilothosts.com)
- **Website:** [www.pilothosts.com](https://www.pilothosts.com)

---

## Screenshots

<img width="2557" height="1438" alt="overview" src="https://github.com/user-attachments/assets/ad0f8f6d-0fd2-41ba-8687-68d48aa8d890" />


---

<div align="center">

Made with care for VMware administrators everywhere.

**[www.pilothosts.com](https://www.pilothosts.com)**

</div>
