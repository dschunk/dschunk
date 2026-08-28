<p align="center">
  <img src="https://raw.githubusercontent.com/dschunk/dschunk/main/assets/profile-banner.svg" alt="David Schunk — Infrastructure, Automation, Operations" width="100%" />
</p>

<p align="center">
  <strong>I build systems the next engineer can understand, operate, and trust.</strong>
</p>

<p align="center">
  Senior IT Engineer focused on infrastructure, automation, operational visibility, and maintainable systems.
</p>

<p align="center">
  <a href="https://www.davidschunk.com/"><img src="https://img.shields.io/badge/davidschunk.com-0B1F3A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Website" /></a>
  <a href="https://www.linkedin.com/in/dschunk/"><img src="https://img.shields.io/badge/LinkedIn-David%20Schunk-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://www.linkedin.com/newsletters/best-practices-for-everyday-it-7075059974573314048/"><img src="https://img.shields.io/badge/Newsletter-Everyday%20IT-C9A227?style=for-the-badge&logo=linkedin&logoColor=white" alt="Best Practices for Everyday IT" /></a>
</p>

<p align="center">
  <a href="https://dschunk.github.io/infrastructure-dashboard/"><img src="https://img.shields.io/badge/LIVE_DEMO-OPEN_OPERATIONS_CENTER-52D69A?style=for-the-badge&logo=githubpages&logoColor=071426" alt="Open live Operations Center demo" /></a>
</p>

## Portfolio snapshot

|  | Public engineering work |
|---:|---|
| **35 + 14** | Standalone Windows tools plus David-branded commands in the installable SchunkOps module |
| **12** | Read-only Microsoft 365, Entra ID, Exchange Online, and Teams security audits |
| **11** | FiveM monitoring, backup, configuration, inventory, logging, and status tools |
| **9** | Runbook, handoff, change, recovery, access, backup, monitoring, retirement, and incident templates |
| **4** | CI workflows validating scripts, manifests, exports, help, safety contracts, and tests |
| **1** | Responsive, dependency-free live Operations Center |

[![Windows CI](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml/badge.svg)](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml)
[![M365 CI](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml/badge.svg)](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml)
[![FiveM CI](https://github.com/dschunk/fivem-server-ops/actions/workflows/validate-powershell.yml/badge.svg)](https://github.com/dschunk/fivem-server-ops/actions/workflows/validate-powershell.yml)

## What I build

| Project | What it does |
|---|---|
| [Windows IT Toolkit](https://github.com/dschunk/windows-it-toolkit) | Thirty-five standalone tools plus **SchunkOps**, an installable module with fourteen Windows operations and incident-response commands |
| [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops) | Twelve least-privilege audits for licensing, MFA, privileged roles, guests, Conditional Access, mailbox forwarding, permissions, domains, and external access |
| [FiveM Server Ops](https://github.com/dschunk/fivem-server-ops) | Eleven tools for monitoring, backup validation, configuration safety, logs, resources, port matrices, status data, and alerts |
| [Infrastructure Dashboard](https://github.com/dschunk/infrastructure-dashboard) | A [live responsive Operations Center](https://dschunk.github.io/infrastructure-dashboard/) built with semantic HTML, CSS, and JavaScript |
| [Build It Like You Won't Be There](https://github.com/dschunk/build-it-like-you-wont-be-there) | Runbooks, handoff standards, and the engineering philosophy behind maintainable systems |

## Flagship workflow: Windows incident evidence

SchunkOps turns “the server is acting weird” into a repeatable evidence
collection and handoff process:

~~~powershell
New-SchunkIncidentBundle -OutputPath C:\IR\INC-0042 -Profile Full
~~~

It captures structured JSON, records collector failures instead of hiding
them, generates SHA-256 integrity hashes, and supports before/after comparison.
Read the [15-minute Windows incident triage](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/INCIDENT-RESPONSE.md).

## Flagship workflow: Microsoft 365 security snapshot

The Microsoft 365 toolkit collects repeatable tenant evidence without hiding
partial failures or taking ownership of authentication:

~~~powershell
Connect-MgGraph -Scopes 'Organization.Read.All','User.Read.All','AuditLog.Read.All','Policy.Read.All','RoleManagement.Read.Directory','Directory.Read.All','Domain.Read.All'
./scripts/Export-M365SecuritySnapshot.ps1 -OutputDirectory C:\Evidence\M365
~~~

The bundle contains structured CSV and JSON, collection metadata, failed-report
details, and SHA-256 integrity hashes. Review the project's
[permission map](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/PERMISSIONS.md)
and [threat model](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/THREAT-MODEL.md).

## Engineering principles

- **Build for the next engineer.** A system is not finished when it works only for its creator.
- **Make failure visible.** Logs, health checks, alerts, and audit trails are product features.
- **Automate carefully.** Safe defaults, dry runs, clear output, and reversible operations matter.
- **Document decisions.** The why is often more valuable than the command that was run.
- **Treat operations as a discipline.** Backups, access control, recovery, and ownership belong in the original design.

## Technologies

![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows%20Server-0078D4?style=flat-square&logo=windows&logoColor=white)
![Microsoft 365](https://img.shields.io/badge/Microsoft%20365-D83B01?style=flat-square&logo=microsoft&logoColor=white)
![Microsoft Entra](https://img.shields.io/badge/Microsoft%20Entra-5E5CE6?style=flat-square&logo=microsoftazure&logoColor=white)
![Exchange Online](https://img.shields.io/badge/Exchange%20Online-0078D4?style=flat-square&logo=microsoftexchange&logoColor=white)
![Microsoft Teams](https://img.shields.io/badge/Microsoft%20Teams-6264A7?style=flat-square&logo=microsoftteams&logoColor=white)
![C Sharp](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![VMware](https://img.shields.io/badge/VMware-607078?style=flat-square&logo=vmware&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)

## Writing about real-world IT

I publish **Best Practices for Everyday IT**, a LinkedIn newsletter about the decisions that make systems easier to operate, secure, document, and hand off.

> If I were gone tomorrow, could another engineer understand what I built, why it exists, how it fails, and how to recover it?

Read the newsletter on [LinkedIn](https://www.linkedin.com/newsletters/best-practices-for-everyday-it-7075059974573314048/) or explore the broader story at [davidschunk.com](https://www.davidschunk.com/).

## More than a résumé

I was born in Smolensk, Russia, adopted as a child, and raised in New Hampshire. Technology became one of the ways I learned to build order, connection, and community. Today I am an IT engineer, infrastructure builder, writer, gamer, and advocate—different parts of one life, not separate identities.

### Start here

If you manage Windows infrastructure, start with [Windows IT Toolkit](https://github.com/dschunk/windows-it-toolkit).  
If you secure a Microsoft 365 tenant, use [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops).  
If you operate a FiveM community, explore [FiveM Server Ops](https://github.com/dschunk/fivem-server-ops).  
If you care about maintainable engineering, read [Build It Like You Won't Be There](https://github.com/dschunk/build-it-like-you-wont-be-there).

Useful feedback, issues, and pull requests are welcome.

