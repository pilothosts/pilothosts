<div align="center">

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://www.pilothosts.com/newlogo/pilothosts_logo_dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://www.pilothosts.com/newlogo/pilothosts_logo_light.svg">
    <img src="https://www.pilothosts.com/newlogo/pilothosts_logo_light.svg" alt="PilotHosts Logo" width="200">
  </picture>

# Changelog

All notable changes to PilotHosts are documented here.
This project follows [Semantic Versioning](https://semver.org/) and the [Keep a Changelog](https://keepachangelog.com/) format.

[![Latest Release](https://img.shields.io/badge/LATEST-v1.1.2-3b82f6?style=for-the-badge&labelColor=0f172a)](https://www.pilothosts.com/release/)
[![Full Release Notes](https://img.shields.io/badge/FULL%20NOTES-pilothosts.com%2Frelease-1f2937?style=flat-square)](https://www.pilothosts.com/release/)

</div>

<br>

<div align="center">

**[v1.1.1](#v111)** · **[v1.1.0](#v110)** · **[v1.0.4](#v104)** · **[v1.0.3](#v103)** · **[v1.0.2](#v102)** · **[v1.0.1](#v101)** · **[v1.0.0](#v100)**

</div>

---

## v1.1.2
<sub>Released 2026-07-15 · Patch Release</sub>
### New Features
- VM Summary now shows every Veeam backup job protecting a VM, with a job switcher and a job count, instead of a single job.
- VM Timeline gained a Data Protection filter, so Veeam backup activity can be viewed on its own.

### 🐛 Fixed
- Backup Protection no longer displays only one arbitrary job for a VM covered by multiple jobs, which could hide a failing backup job behind a healthy one; the panel now reflects the least-protected job.
- Right-sizing recommendations are more accurate: a clear CPU or memory bottleneck is no longer under-scored by the other, idle metric, and memory-reduction suggestions are sized to real peak usage to avoid swap or out-of-memory risk.
- VM configuration history no longer reports misleading "provisioned storage grew" entries that came from internal storage accounting rather than an actual disk change.
- Fixed a crash that could occur when opening the Executive Summary and Retired VM Candidates reports.
- The configuration history pagination control is now hidden when there is only a single page of changes.
- Backup Servers: the add button is now labeled "Add Backup Server" and placed above the list; unified the Add button appearance across the Environments, Assets and Backup Servers pages.

  
## v1.1.1
<sub>Released 2026-07-15 · Patch Release</sub>

### 🐛 Fixed
- Fixed a report page crash caused by comparing timezone-aware and timezone-naive timestamps.Various UI/UX improvements.

## v1.1.0
<sub>Released 2026-07-07 · Feature Release</sub>

### 🛡️ Added: Backup & Data Protection (Veeam)
- **Protection Dashboard:** a new Data Protection section showing backup coverage, freshness, ransomware/malware scan status, job health, and repository capacity at a glance.
- **Unprotected VMs Report:** instantly see which VMs were never backed up or have stale backups, with datacenter and cluster context.
- **Backup Jobs View:** full job list with schedule, last run result, retention policy, assigned proxy, and a drill-down into each job's backup chain and contents.
- **Backup SLA Compliance:** define policies (max RPO, minimum restore points, required success) and see exactly which VMs are in or out of compliance.
- **Veeam Proxy Sizing:** calculates the backup proxy capacity your environment actually needs from real protected data volume and measured change rate, compares it to what's deployed, and flags when more capacity is required.
- **Backup-Aware VM Creation:** new VMs can be assigned to an existing Veeam backup job right from the deploy wizard, so nothing goes live unprotected.
- **Pilot Assistant, Backup-Aware:** ask about unprotected VMs, recent backup failures, or SLA status alongside your VMware and Kubernetes questions.

### ⚙️ Improved
- **Cost & Waste Insights:** the Protection page now surfaces newly-added unprotected VMs, zombie VMs still consuming backup license and storage, and stuck Veeam snapshots.
- **Immutable Backups View:** shows ransomware-protection coverage per VM and per repository.
- **Backup Proxy Visibility:** each backup job now shows which proxy it runs on, including when it's falling back to the built-in default proxy.

---

## v1.0.4
<sub>Released 2026-07-03 · Patch Release</sub>

### 🐛 Fixed
- Resolved several bug fixes improving overall stability and reliability.

---

## v1.0.3
<sub>Released 2026-07-02 · Patch Release</sub>

### 🐛 Fixed
- Resolved several bug fixes improving overall stability and reliability.

---

## v1.0.2
<sub>Released 2026-07-01 · Patch Release</sub>

### ⚙️ Improved
- **Renewal Guidance (Licenses Page):** a brief renewal reminder has been added below the license holder name, explaining the 7-day grace period and recommending renewal at least 30 days before expiry to avoid any service interruption.
- **Visual Polish (Licenses Page):** typography and layout across the Licenses page have been refined: stat values (expiry date, host usage, license type, support, license key) now use consistent font weight and size, improving readability and visual balance in both light and dark themes.
- **Appliance Version Badge (Sidebar):** the current appliance version (e.g., v1.0.2) is now displayed directly in the sidebar, just above your user profile. You no longer need to navigate to Configuration to check the running version.
- **License Verification Reliability:** license validity checks are now more consistent across all usage patterns, including during active dashboard sessions.
- **Update Infrastructure:** internal improvements to how the appliance communicates with the update service, enabling better diagnostics and faster support response when issues arise.

---

## v1.0.1
<sub>Released 2026-06-29 · Patch Release</sub>

### ⚙️ Improved
- Refreshed UI/UX across the appliance interface for a cleaner, more consistent experience.

### 🐛 Fixed
- Resolved several bug fixes improving overall stability and reliability.

---

## v1.0.0
<sub>Released 2026-06-01 · Initial Release</sub>

### ✨ Added
- Initial PilotHosts appliance release for hybrid VMware, Kubernetes and OpenShift visibility.
- VMware vCenter inventory, host and VM metrics, snapshot visibility and cleanup workflows.
- Read-only Kubernetes and OpenShift context for health, inventory and risk reporting.
- Local appliance deployment with API-based integrations and encrypted credentials.

### 🔒 Security
- Data stays on premises inside the PilotHosts appliance.
- Integrations use official APIs and do not require agents on managed platforms.

---

<div align="center">

For the full, browsable release history see **[pilothosts.com/release](https://www.pilothosts.com/release/)**.

</div>
