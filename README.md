<p align="center">
  <img src="https://raw.githubusercontent.com/dschunk/dschunk/main/assets/profile-banner.svg?v=20260829-2" alt="David Schunk — Infrastructure, Automation, Operations" width="100%" />
</p>

<p align="center">
  <strong>Windows • Microsoft 365 • Identity • Infrastructure • Incident Response</strong>
</p>

<p align="center">
  Open-source tools and operational playbooks built for the people who actually have to support the environment.<br>
  <strong>Help desk can use them. Sysadmins can automate them. Senior engineers can audit and extend them.</strong>
</p>

<p align="center">
  <a href="https://www.davidschunk.com/"><img src="https://img.shields.io/badge/davidschunk.com-0B1F3A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Website" /></a>
  <a href="https://www.linkedin.com/in/dschunk/"><img src="https://img.shields.io/badge/LinkedIn-David%20Schunk-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://www.linkedin.com/newsletters/best-practices-for-everyday-it-7075059974573314048/"><img src="https://img.shields.io/badge/Newsletter-Everyday%20IT-C9A227?style=for-the-badge&logo=linkedin&logoColor=white" alt="Best Practices for Everyday IT" /></a>
</p>

> **Personal-project boundary:** Unless a repository explicitly states otherwise, the work showcased on this personal GitHub profile is maintained as independent personal, open-source, or community work. No affiliation with or endorsement by any current or former employer is implied. These repositories are not intended to contain employer confidential or proprietary information, non-public internal configurations, customer data, credentials, or employer work product.

# IT Operations Center

If you work in IT, start with the problem in front of you.

| Role / problem | Start here | What you get |
|---|---|---|
| **Help desk / desktop support** | [Windows IT Toolkit — Help Desk Field Guide](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/HELPDESK.md) | Five-minute endpoint triage, DNS, domain trust, SMB, RDP, admin checks, escalation evidence |
| **Windows sysadmin** | [Windows IT Toolkit](https://github.com/dschunk/windows-it-toolkit) | 35 standalone tools + the 20-command **SchunkOps** PowerShell module |
| **AD / identity engineer** | [SchunkOps Windows](https://github.com/dschunk/windows-it-toolkit) | Domain trust, DC reachability, replication health, stale objects, GPO, time, DNS, local admin review |
| **Microsoft 365 admin** | [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops) | 12 read-only Entra, Exchange Online, Teams, licensing, MFA, guest, CA, and forwarding audits |
| **Incident responder** | [15-minute Windows incident triage](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/INCIDENT-RESPONSE.md) | Structured JSON evidence, collector status, timestamps, SHA-256 hashes, before/after comparison |
| **Infrastructure / operations engineer** | [Build It Like You Won't Be There](https://github.com/dschunk/build-it-like-you-wont-be-there) | Runbook, recovery, monitoring, access, change, ownership, and handoff templates |
| **Platform / dashboard builder** | [Infrastructure Dashboard](https://github.com/dschunk/infrastructure-dashboard) | A live operations-center interface and public implementation example |

## The command I want help desk to know

```powershell
Import-Module SchunkOps
Get-SchunkEndpointTriage
```

That one command gives a technician a structured first look at uptime, memory pressure, disks, active IP/DNS/gateway/DHCP configuration, domain membership, machine secure channel, pending reboot state, Windows Time source, stopped automatic services, and recent System/Application critical and error events.

Then move up the stack instead of guessing:

```powershell
# Trust relationship / domain issue
Get-SchunkDomainTrustStatus -TestPorts

# Works by IP, fails by name
Test-SchunkDnsClient -Name fileserver.contoso.com

# Senior AD check
Get-SchunkADReplicationHealth

# Privilege review
Get-SchunkLocalAdministrator -ComputerName PC001,PC002,SERVER01

# Server / incident evidence
New-SchunkIncidentBundle -OutputPath C:\IR\INC-0042 -Profile Full
```

The operating model is deliberate: **collect first, change second, document always.**

## What is actually here

| Delivered | Public proof |
|---:|---|
| **35** | Standalone Windows administration, security, networking, identity, and diagnostic tools |
| **20** | Installable commands in the **SchunkOps** Windows PowerShell module |
| **12** | Read-only Microsoft 365, Entra ID, Exchange Online, and Teams security audits |
| **11** | FiveM monitoring, backup, configuration, inventory, logging, and status tools |
| **9** | Production-ready runbook, recovery, access, change, monitoring, and handoff templates |
| **5+** | GitHub Actions workflows enforcing parsing, analysis, tests, safety contracts, and web validation |
| **2** | Live public systems: an Operations Center demo and a production Cloudflare community platform |

[![Windows CI](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml/badge.svg)](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml)
[![SchunkOps CI](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-module.yml/badge.svg)](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-module.yml)
[![M365 CI](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml/badge.svg)](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml)
[![FiveM CI](https://github.com/dschunk/fivem-server-ops/actions/workflows/validate-powershell.yml/badge.svg)](https://github.com/dschunk/fivem-server-ops/actions/workflows/validate-powershell.yml)

## Flagship: SchunkOps for Windows

[Windows IT Toolkit](https://github.com/dschunk/windows-it-toolkit) is the main field kit: 35 standalone scripts for grab-and-run administration plus a curated 20-command module for repeatable operations.

### Help desk / endpoint

- `Get-SchunkEndpointTriage`
- `Get-SchunkDomainTrustStatus`
- `Test-SchunkDnsClient`
- `Get-SchunkDiskPressure`
- `Get-SchunkLocalAdministrator`
- `Get-SchunkPendingReboot`

### Windows / server operations

- `Get-SchunkServerHealth`
- `Get-SchunkServiceFailure`
- `Get-SchunkEventTriage`
- `Get-SchunkListeningPort`
- `Get-SchunkScheduledTaskAudit`
- `Get-SchunkWindowsUpdateHistory`

### AD / identity

- `Get-SchunkADReplicationHealth`
- standalone AD health, stale user/computer, GPO, DC port, DNS, DHCP, and time-synchronization tools

### Incident response

```powershell
New-SchunkIncidentBundle -OutputPath C:\IR\INC-0042 -Profile Full
```

The bundle writes separate JSON evidence files, records collector success/failure, timestamps the collection, generates SHA-256 integrity hashes, and can be compared against a post-remediation capture:

```powershell
Compare-SchunkIncidentBundle `
    -ReferencePath C:\IR\INC-0042 `
    -DifferencePath C:\IR\INC-0042-After
```

This is the kind of output I want attached to an escalation instead of a screenshot of Task Manager and “server seems weird.”

## SchunkOps Microsoft 365

[SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops) is intentionally read-only. It expects the operator to authenticate through Microsoft's supported modules, documents required permissions, returns objects, and does not silently request broader scopes or modify tenant state.

It answers operational questions such as:

- Who has privileged Entra roles?
- Who is missing MFA registration?
- Which enabled users are inactive?
- Which guest accounts need review?
- What do Conditional Access policies target?
- Which mailboxes or inbox rules forward externally?
- Who has access to shared mailboxes?
- How is Teams external access configured?
- Can the tenant be captured as a timestamped, hashed security snapshot?

```powershell
Connect-MgGraph -Scopes 'User.Read.All','AuditLog.Read.All'
./scripts/Get-M365InactiveUser.ps1 -InactiveDays 90 |
    Export-Csv ./inactive-users.csv -NoTypeInformation
```

For broader evidence collection:

```powershell
./scripts/Export-M365SecuritySnapshot.ps1 -OutputDirectory C:\Evidence\M365
```

## Featured engineering

| Project | Engineering value |
|---|---|
| [Windows IT Toolkit](https://github.com/dschunk/windows-it-toolkit) | Help desk through senior-engineer Windows operations: 35 standalone tools, 20 SchunkOps commands, field guides, evidence bundles, Pester, PSScriptAnalyzer, and Windows CI |
| [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops) | Twelve least-privilege audits for licensing, MFA, privileged roles, guests, Conditional Access, forwarding, permissions, domains, and external access |
| [Build It Like You Won't Be There](https://github.com/dschunk/build-it-like-you-wont-be-there) | Operational templates and the engineering philosophy behind systems another person can safely inherit |
| [Infrastructure Dashboard](https://github.com/dschunk/infrastructure-dashboard) | A [live responsive Operations Center](https://dschunk.github.io/infrastructure-dashboard/) built with semantic HTML, CSS, and JavaScript |
| [FiveM Server Ops](https://github.com/dschunk/fivem-server-ops) | Eleven production-minded tools for Windows-hosted FiveM monitoring, backup validation, configuration safety, logs, resources, ports, and alerts |
| [Russian Adoptees Organization](https://github.com/dschunk/russian-adoptees) | A [production public platform](https://russianadoptees.com/) combining Cloudflare Workers, secure contact delivery, public resources, governance, community infrastructure, and automated validation |

## How I engineer

- **Build for the next engineer.** A system is not finished when it works only for its creator.
- **Make failure visible.** Logs, health checks, alerts, audit trails, and partial-failure reporting are product features.
- **Read-only is a feature.** Diagnostic tooling should not quietly become remediation tooling.
- **Return objects, not screenshots.** People can read objects; engineers can pipe them; automation can serialize them.
- **Automate with restraint.** Least privilege, dry runs, validation, and reversible operations matter.
- **Treat documentation as infrastructure.** The why, ownership, failure modes, and recovery path belong beside the code.

## Technologies

![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows%20Server-0078D4?style=flat-square&logo=windows&logoColor=white)
![Microsoft 365](https://img.shields.io/badge/Microsoft%20365-D83B01?style=flat-square&logo=microsoft&logoColor=white)
![Microsoft Entra](https://img.shields.io/badge/Microsoft%20Entra-5E5CE6?style=flat-square&logo=microsoftazure&logoColor=white)
![Exchange Online](https://img.shields.io/badge/Exchange%20Online-0078D4?style=flat-square&logo=microsoftexchange&logoColor=white)
![C Sharp](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![VMware](https://img.shields.io/badge/VMware-607078?style=flat-square&logo=vmware&logoColor=white)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare%20Workers-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

## Beyond the toolkits

I also build production platforms and publish **Best Practices for Everyday IT**, a LinkedIn newsletter about the decisions that make systems easier to operate, secure, document, recover, and hand off.

> If I were gone tomorrow, could another engineer understand what I built, why it exists, how it fails, and how to recover it?

I was born in Smolensk, Russia, adopted as a child, and raised in New Hampshire. Technology became one of the ways I learned to build order, connection, and community. Today I work across infrastructure, automation, writing, open source, and community projects.

Read [Best Practices for Everyday IT](https://www.linkedin.com/newsletters/best-practices-for-everyday-it-7075059974573314048/), connect on [LinkedIn](https://www.linkedin.com/in/dschunk/), or explore the broader story at [davidschunk.com](https://www.davidschunk.com/).

---

**If one of these tools saves you time, star the repository, open an issue, improve the docs, or send a pull request.** Useful feedback and responsible reuse are welcome.
