<p align="center">
  <img src="https://raw.githubusercontent.com/dschunk/dschunk/main/assets/profile-banner.svg?v=20260829-2" alt="David Schunk — Infrastructure, Automation, Operations" width="100%" />
</p>

<p align="center">
  <strong>I build systems the next engineer can understand, operate, secure, and trust.</strong>
</p>

<p align="center">
  Senior IT Engineer building Windows and Microsoft 365 automation, incident-response tooling,<br>
  operational dashboards, and production platforms for real organizations and communities.
</p>

<p align="center">
  <a href="https://www.davidschunk.com/"><img src="https://img.shields.io/badge/davidschunk.com-0B1F3A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Website" /></a>
  <a href="https://www.linkedin.com/in/dschunk/"><img src="https://img.shields.io/badge/LinkedIn-David%20Schunk-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://www.linkedin.com/newsletters/best-practices-for-everyday-it-7075059974573314048/"><img src="https://img.shields.io/badge/Newsletter-Everyday%20IT-C9A227?style=for-the-badge&logo=linkedin&logoColor=white" alt="Best Practices for Everyday IT" /></a>
</p>

<p align="center">
  <a href="https://dschunk.github.io/infrastructure-dashboard/"><img src="https://img.shields.io/badge/LIVE_DEMO-OPERATIONS_CENTER-52D69A?style=for-the-badge&logo=githubpages&logoColor=071426" alt="Open live Operations Center demo" /></a>
  <a href="https://russianadoptees.com/"><img src="https://img.shields.io/badge/LIVE_PLATFORM-RUSSIAN_ADOPTEES-D4A72C?style=for-the-badge&logo=cloudflare&logoColor=071426" alt="Open Russian Adoptees Organization" /></a>
</p>

## Engineering portfolio

| Delivered | Public proof |
|---:|---|
| **35** | Standalone Windows administration, security, networking, identity, and diagnostic tools |
| **14** | Installable commands in the David-branded **SchunkOps** PowerShell module |
| **12** | Read-only Microsoft 365, Entra ID, Exchange Online, and Teams security audits |
| **11** | FiveM monitoring, backup, configuration, inventory, logging, and status tools |
| **9** | Production-ready runbook, recovery, access, change, monitoring, and handoff templates |
| **5** | GitHub Actions workflows enforcing parsing, analysis, tests, safety contracts, and web validation |
| **2** | Live public systems: an Operations Center demo and a production Cloudflare community platform |

[![Windows CI](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml/badge.svg)](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml)
[![M365 CI](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml/badge.svg)](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml)
[![FiveM CI](https://github.com/dschunk/fivem-server-ops/actions/workflows/validate-powershell.yml/badge.svg)](https://github.com/dschunk/fivem-server-ops/actions/workflows/validate-powershell.yml)
[![RAO Site CI](https://github.com/dschunk/russian-adoptees/actions/workflows/validate-site.yml/badge.svg)](https://github.com/dschunk/russian-adoptees/actions/workflows/validate-site.yml)

## Featured engineering

| Project | Engineering value |
|---|---|
| [Windows IT Toolkit](https://github.com/dschunk/windows-it-toolkit) | Thirty-five standalone tools plus the installable **SchunkOps** module for Windows operations and incident response |
| [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops) | Twelve least-privilege audits for licensing, MFA, privileged roles, guests, Conditional Access, forwarding, permissions, domains, and external access |
| [Russian Adoptees Organization](https://github.com/dschunk/russian-adoptees) | A [production public platform](https://russianadoptees.com/) combining Cloudflare Workers, static assets, secure email delivery, public resources, governance records, community infrastructure, and automated validation |
| [FiveM Server Ops](https://github.com/dschunk/fivem-server-ops) | Eleven production-minded tools for Windows-hosted FiveM monitoring, backup validation, configuration safety, logs, resources, ports, and alerts |
| [Infrastructure Dashboard](https://github.com/dschunk/infrastructure-dashboard) | A [live responsive Operations Center](https://dschunk.github.io/infrastructure-dashboard/) built with semantic HTML, CSS, and JavaScript |
| [Build It Like You Won't Be There](https://github.com/dschunk/build-it-like-you-wont-be-there) | Operational templates and the engineering philosophy behind systems another person can safely inherit |

## Production platform: Russian Adoptees Organization

<table>
  <tr>
    <td width="72%">
      I founded the Russian Adoptees Organization and built its public technology platform from policy documents and community needs into a production system.<br><br>
      <strong>The platform includes:</strong> twelve public content routes, Russian citizenship and consular starting guides, official-source law updates, a public document archive, organizational governance pages, Discord and Facebook community entry points, a secure contact workflow, role-based email identities, site-wide official branding, SEO metadata, and GitHub Actions validation.<br><br>
      The contact Worker validates origin and payload size, filters basic bot submissions, keeps private delivery addresses out of source control, and reports configuration health without exposing secrets.
    </td>
    <td width="28%" align="center">
      <a href="https://russianadoptees.com/"><img src="https://raw.githubusercontent.com/dschunk/russian-adoptees/main/public/assets/rao-seal.svg" width="170" alt="Russian Adoptees Organization official seal" /></a><br>
      <strong><a href="https://russianadoptees.com/">Visit the live platform</a></strong>
    </td>
  </tr>
</table>

## Flagship workflow: Windows incident evidence

SchunkOps turns “the server is acting weird” into a repeatable evidence collection and handoff process:

```powershell
New-SchunkIncidentBundle -OutputPath C:\IR\INC-0042 -Profile Full
```

The bundle captures structured JSON, records collector failures instead of hiding them, generates SHA-256 integrity hashes, and supports before-and-after comparison. Start with the [15-minute Windows incident triage](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/INCIDENT-RESPONSE.md).

## Flagship workflow: Microsoft 365 security evidence

The Microsoft 365 toolkit collects tenant evidence without silently changing the environment or taking ownership of authentication:

```powershell
Connect-MgGraph -Scopes 'User.Read.All','AuditLog.Read.All'
./scripts/Get-M365InactiveUser.ps1 -InactiveDays 90 |
    Export-Csv ./inactive-users.csv -NoTypeInformation
```

For broader evidence collection, `Export-M365SecuritySnapshot.ps1` creates structured CSV and JSON, collection metadata, failed-report details, and SHA-256 hashes. Review the [permission map](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/PERMISSIONS.md) and [threat model](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/THREAT-MODEL.md).

## How I engineer

- **Build for the next engineer.** A system is not finished when it works only for its creator.
- **Make failure visible.** Logs, health checks, alerts, audit trails, and partial-failure reporting are product features.
- **Automate with restraint.** Least privilege, read-only defaults, dry runs, validation, and reversible operations matter.
- **Treat documentation as infrastructure.** The why, ownership, failure modes, and recovery path belong beside the code.
- **Connect technical work to people.** Infrastructure matters because someone relies on it—an operator, an organization, or a community.

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
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=111)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)

## Writing, leadership, and the person behind the code

I publish **Best Practices for Everyday IT**, a LinkedIn newsletter about the decisions that make systems easier to operate, secure, document, recover, and hand off.

> If I were gone tomorrow, could another engineer understand what I built, why it exists, how it fails, and how to recover it?

I was born in Smolensk, Russia, adopted as a child, and raised in New Hampshire. Technology became one of the ways I learned to build order, connection, and community. Today I am a senior IT engineer, infrastructure builder, founder, writer, gamer, podcaster, and advocate—different parts of one life, not separate identities.

Read [Best Practices for Everyday IT](https://www.linkedin.com/newsletters/best-practices-for-everyday-it-7075059974573314048/), connect on [LinkedIn](https://www.linkedin.com/in/dschunk/), or explore the broader story at [davidschunk.com](https://www.davidschunk.com/).

### Start here

- Windows infrastructure: [Windows IT Toolkit](https://github.com/dschunk/windows-it-toolkit)
- Microsoft 365 security: [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops)
- Production web platform: [Russian Adoptees Organization](https://github.com/dschunk/russian-adoptees)
- Game-server operations: [FiveM Server Ops](https://github.com/dschunk/fivem-server-ops)
- Maintainable operations: [Build It Like You Won't Be There](https://github.com/dschunk/build-it-like-you-wont-be-there)

Useful feedback, issues, pull requests, citations, and responsible reuse are welcome.
