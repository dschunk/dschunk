<p align="center">
  <img src="https://raw.githubusercontent.com/dschunk/dschunk/main/assets/profile-banner.svg?v=20260829-2" alt="David Schunk — Infrastructure, Automation, Operations" width="100%" />
</p>

<p align="center">
  <strong>Windows • Microsoft 365 • Identity • Infrastructure • Automation • Operations</strong>
</p>

<p align="center">
  I build practical systems, tools, documentation, and public field guides for the people who have to keep technology running.
</p>

<p align="center">
  <a href="https://www.davidschunk.com/"><img src="https://img.shields.io/badge/davidschunk.com-0B1F3A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="DavidSchunk.com" /></a>
  <a href="https://everydayittips.com/"><img src="https://img.shields.io/badge/Everyday%20IT%20Tips-1F5C42?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Everyday IT Tips" /></a>
  <a href="https://www.linkedin.com/in/dschunk/"><img src="https://img.shields.io/badge/LinkedIn-David%20Schunk-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
</p>

> **Personal-project boundary:** Unless a repository explicitly states otherwise, the work showcased here is maintained as independent personal, open-source, editorial, or community work. No affiliation with or endorsement by any current or former employer is implied. These repositories are not intended to contain employer confidential or proprietary information, non-public internal configurations, customer data, credentials, or employer work product.

# Build systems the next engineer can inherit.

A working system is not finished if only one person understands it.

The engineering model across these projects is simple:

**Collect first. Change second. Document always.**

## Start here

| Area | Project | What it is |
|---|---|---|
| **Windows / AD / infrastructure** | [Windows IT Toolkit / SchunkOps](https://github.com/dschunk/windows-it-toolkit) | 35 standalone PowerShell tools plus a 28-command module for endpoint, server, AD, Kerberos, GPO, DNS/DHCP, certificates, clusters, vSphere, and incident evidence |
| **Microsoft 365 / Entra / Exchange** | [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops) | 20 read-only support and engineering tools for identities, licenses, sign-ins, service health, mailboxes, privileged access, Conditional Access, guests, Teams, and tenant evidence |
| **Practical IT writing** | [Everyday IT Tips](https://everydayittips.com/) | Searchable field guides for Windows, Active Directory, Windows Server, security, infrastructure, troubleshooting, and IT operations |
| **Operational discipline** | [Build It Like You Won't Be There Tomorrow](https://github.com/dschunk/build-it-like-you-wont-be-there) | Runbook, recovery, access, change, monitoring, handoff, backup, and decommissioning templates |
| **Interface / operations design** | [Infrastructure Dashboard](https://github.com/dschunk/infrastructure-dashboard) | Sanitized, dependency-free operations-center demonstration using synthetic telemetry |
| **Community infrastructure** | [Russian Adoptees Organization](https://github.com/dschunk/russian-adoptees) | Production Cloudflare platform with secure public contact, resources, governance, community infrastructure, and automated validation |

## SchunkOps for Windows

```powershell
Import-Module SchunkOps

# First look at a Windows machine
Get-SchunkEndpointTriage

# Find unhealthy systems across a fleet
Get-SchunkFleetHealth -ComputerName server01,server02,server03

# Trace Active Directory account lockouts
Get-SchunkAccountLockoutTrace -Identity jsmith -LookbackHours 24

# Review recent Group Policy changes
Get-SchunkGpoChangeAudit -SinceDays 14 -IncludeFingerprint

# Preserve incident evidence
New-SchunkIncidentBundle -OutputPath C:\IR\INC-0042 -Profile Full
```

[![Windows CI](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml/badge.svg)](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml)
[![SchunkOps CI](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-module.yml/badge.svg)](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-module.yml)
[![M365 CI](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml/badge.svg)](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml)

## Everyday IT Tips

**Best Practices for Everyday IT** now has a permanent home at [EverydayITtips.com](https://everydayittips.com/).

The publication is built around practical, repeatable work rather than vendor marketing or generic advice. Current coverage includes:

- Windows 11 and Windows Server
- Active Directory and Group Policy
- DNS and DHCP
- RDP and Windows troubleshooting
- SMB, NTFS, storage, and Hyper-V
- BitLocker, Windows LAPS, and firewall administration
- backup and restore testing
- documentation and operational handoff

Start with the [Windows Administration Hub](https://everydayittips.com/topics/windows/) or browse [all field guides](https://everydayittips.com/guides/).

The LinkedIn newsletter remains a distribution channel; the website is the permanent publication and archive.

## Engineering principles

- **Build for the next engineer.** The system should survive its creator being unavailable.
- **Make failure visible.** Logs, alerts, health checks, audit trails, and partial-failure reporting are features.
- **Read-only is a feature.** Diagnostic tooling should not quietly become remediation tooling.
- **Return objects, not screenshots.** Operators can read them; engineers can pipe them; automation can serialize them.
- **Automate with restraint.** Least privilege, validation, reversible actions, and explicit scope matter.
- **Treat documentation as infrastructure.** Ownership, dependencies, failure modes, recovery, and handoff belong beside the code.

## Core technologies

`PowerShell` · `Windows Server` · `Active Directory` · `Group Policy` · `Microsoft 365` · `Microsoft Entra` · `Exchange Online` · `.NET` · `VMware` · `Cloudflare Workers` · `GitHub Actions`

## Beyond the toolkits

I work across infrastructure, automation, writing, open source, and community projects. I was born in Smolensk, Russia, adopted as a child, and raised in New Hampshire.

The broader portfolio is at [davidschunk.com](https://www.davidschunk.com/). Technical writing lives at [Everyday IT Tips](https://everydayittips.com/). I’m also on [LinkedIn](https://www.linkedin.com/in/dschunk/).

---

**If something here saves you time, use it responsibly, improve the documentation, open an issue, or send a pull request.**
