<p align="center">
  <img src="https://raw.githubusercontent.com/dschunk/dschunk/main/assets/profile-banner.svg" alt="David Schunk — Windows Infrastructure, Automation, Operations, and Technical Writing" width="100%" />
</p>

<p align="center">
  <strong>Senior IT Engineer · Windows Infrastructure · Automation · Operations · Technical Writing</strong>
</p>

<p align="center">
  I build practical tools, field guides, and operating standards for people who have to keep real systems running.
</p>

<p align="center">
  <a href="https://www.davidschunk.com/">Portfolio</a> ·
  <a href="https://everydayittips.com/">Everyday IT Tips</a> ·
  <a href="https://www.linkedin.com/in/dschunk/">LinkedIn</a> ·
  <a href="https://meritpages.com/DavidSchunk">Academic & career record</a>
</p>

---

## Choose your path

| If you are... | Start here | What you will find |
|---|---|---|
| **New to IT or PowerShell** | [Learning Paths](docs/LEARNING-PATHS.md) | Safe starting points, foundational concepts, guided labs, and a progression from first-line support to systems engineering |
| **Help desk / desktop support** | [SchunkOps Quick Start](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/QUICKSTART.md) | Endpoint triage, DNS, trust, RDP, SMB, reboot state, event evidence, and escalation-ready output |
| **Windows / infrastructure engineer** | [Windows IT Toolkit / SchunkOps](https://github.com/dschunk/windows-it-toolkit) | Read-only-first diagnostics for Windows Server, AD, GPO, Kerberos, DNS/DHCP, certificates, clusters, vSphere, and incident evidence |
| **Microsoft 365 / Entra admin** | [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops) | Twenty read-only tools for identity, licensing, sign-ins, mailboxes, service health, Conditional Access, Teams, and security review |
| **Instructor / professor** | [Teaching & Classroom Guide](docs/CLASSROOM.md) | Assignment ideas, lab sequences, learning objectives, discussion prompts, and ways to use the repositories safely in class |
| **Engineering leader / architect** | [Engineering Standards](docs/ENGINEERING-STANDARDS.md) | Operational design principles, handoff expectations, evidence-first troubleshooting, recovery, change, and maintainability standards |
| **Looking for the whole portfolio** | [Repository Map](docs/REPOSITORY-MAP.md) | A curated index of technical, writing, research, community, and case-study projects |

> **Core principle:** Build systems the next engineer can inherit.

## Flagship resources

### Windows IT Toolkit / SchunkOps

[![Windows CI](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml/badge.svg)](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-powershell.yml)
[![Module CI](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-module.yml/badge.svg)](https://github.com/dschunk/windows-it-toolkit/actions/workflows/validate-module.yml)
[![Latest release](https://img.shields.io/github/v/release/dschunk/windows-it-toolkit?label=SchunkOps)](https://github.com/dschunk/windows-it-toolkit/releases/latest)

A Windows operations toolkit built around structured evidence, safe defaults, and reusable PowerShell objects.

```powershell
git clone https://github.com/dschunk/windows-it-toolkit.git
Import-Module .\windows-it-toolkit\module\SchunkOps\SchunkOps.psd1

# First look at a Windows machine
Get-SchunkEndpointTriage

# Find unhealthy systems across a fleet
Get-SchunkFleetHealth -ComputerName server01,server02,server03

# Trace an AD account lockout
Get-SchunkAccountLockoutTrace -Identity jsmith -LookbackHours 24

# Preserve incident evidence before making changes
New-SchunkIncidentBundle -OutputPath C:\IR\INC-0042 -Profile Full
```

**Start by role:** [Help Desk](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/HELPDESK.md) · [Quick Start](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/QUICKSTART.md) · [Incident Response](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/INCIDENT-RESPONSE.md) · [Senior Engineer](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/SENIOR-ENGINEER.md)

### SchunkOps Microsoft 365

[![M365 CI](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml/badge.svg)](https://github.com/dschunk/microsoft-365-ops/actions/workflows/validate.yml)

Read-only-first PowerShell tooling for Microsoft 365 and Entra operations: identities, licenses, sign-ins, service health, privileged access, mailbox delegation, forwarding, transport rules, Conditional Access, Teams, guests, and tenant evidence.

**Start by role:** [Help Desk](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/HELPDESK.md) · [Operator Checklist](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/OPERATOR-CHECKLIST.md) · [Senior Admin](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/SENIOR-ADMIN.md) · [Threat Model](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/THREAT-MODEL.md)

### Build It Like You Won't Be There Tomorrow

Reusable operational templates for teams that want systems to survive turnover, incidents, vacations, promotions, and the original engineer moving on.

- [System Runbook](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/system-runbook.md)
- [Engineering Handoff Checklist](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/handoff-checklist.md)
- [Disaster Recovery Plan](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/disaster-recovery-plan.md)
- [Backup and Restore Standard](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/backup-standard.md)
- [Blameless Post-Incident Review](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/post-incident-review.md)

## Learn, use, teach, improve

The repositories are designed to work at more than one level.

**Beginners** can follow guided examples and learn what evidence matters before changing a system.  
**Working engineers** can run focused tools, pipe structured output, and adapt the patterns to real environments.  
**Educators** can use the labs, templates, discussion prompts, and citation metadata in coursework.  
**Engineering leaders** can use the operational standards as review questions for production readiness and handoff.

- [Learning paths](docs/LEARNING-PATHS.md)
- [Teaching & classroom use](docs/CLASSROOM.md)
- [Engineering standards](docs/ENGINEERING-STANDARDS.md)
- [Repository map](docs/REPOSITORY-MAP.md)

## Quality bar

For the core engineering repositories, I try to make the quality signals visible rather than implied:

- **safe defaults** — diagnostic and read-only behavior first;
- **structured output** — data that can be read, piped, serialized, tested, and archived;
- **documented privilege requirements** — operators should know what access a tool needs before running it;
- **tests and CI** — validation on pushes and pull requests;
- **security guidance** — no credentials, private tenant data, internal host inventories, or proprietary information in public issues;
- **contribution guidance** — focused changes, non-production testing, sanitized examples, and explicit failure behavior;
- **versioning and release notes** where a project is distributed as a reusable tool;
- **citation metadata** on repositories intended to be referenced in research, education, or formal technical material.

Read the full [Engineering Standards](docs/ENGINEERING-STANDARDS.md).

## Follow active work

If you want to come back for what changed rather than reread the profile:

- **[SchunkOps releases](https://github.com/dschunk/windows-it-toolkit/releases)** — versioned Windows operations releases and release notes.
- **[Windows IT Toolkit roadmap](https://github.com/dschunk/windows-it-toolkit/blob/main/ROADMAP.md)** — planned improvements and areas under active development.
- **[Microsoft 365 Ops roadmap](https://github.com/dschunk/microsoft-365-ops/blob/main/ROADMAP.md)** — planned tenant, identity, Exchange, and security work.
- **[Everyday IT Tips](https://everydayittips.com/)** — the permanent stream of practical field guides and technical writing.
- **[GitHub profile repository map](docs/REPOSITORY-MAP.md)** — the maintained index when new public projects are added.

For code projects, use **Releases** when you need stable version history and **Watch** when you want GitHub notifications for repository activity.

## Practical IT writing

I publish [Everyday IT Tips](https://everydayittips.com/) as the permanent home for field guides on:

`Windows` · `Windows Server` · `Active Directory` · `Group Policy` · `DNS/DHCP` · `PowerShell` · `Microsoft 365` · `security` · `virtualization` · `backup/recovery` · `troubleshooting`

Recent starting points:

- [Windows Server post-build checklist](https://everydayittips.com/guides/windows-server-post-build-checklist/)
- [Windows network troubleshooting toolkit](https://everydayittips.com/guides/windows-network-troubleshooting-toolkit/)
- [PowerShell disk-space triage](https://everydayittips.com/guides/powershell-disk-space-triage/)
- [Windows file server: DFS, FSRM, VSS, permissions, and recovery](https://everydayittips.com/guides/windows-file-server-dfs-fsrm-vss/)

## Research

### [Checks and Balances for Artificial Intelligence](https://www.davidschunk.com/research/ai-governance)

A risk-tiered governance framework focused on human agency, accountability, evidence, deployment controls, independent review, and stronger safeguards as capability and consequence increase.

[Canonical paper](https://www.davidschunk.com/research/ai-governance) · [Source-controlled copy](research/checks-and-balances-for-artificial-intelligence.md)

## Community work

Technology is not the only thing I work on.

- [Voice of Adoptees](https://voiceofadoptees.com/) — long-form conversations centered on adoptee voices and lived experience.
- [Russian Adoptees Organization](https://russianadoptees.com/) — community resources and infrastructure for adoptees from Russia and the former Soviet Union.

## About

I'm David Schunk, a Senior IT Engineer and Champlain College Class of 2017 graduate based in New Hampshire. My work spans Windows infrastructure, systems administration, automation, networking, virtualization, cloud technologies, Microsoft 365, identity, and cybersecurity.

I care about a specific kind of engineering: **systems that are understandable under pressure, recoverable after failure, and maintainable by someone other than the person who built them.**

That same idea drives the tools, documentation, field guides, and operational templates in this profile.

<p align="center">
  <a href="https://www.davidschunk.com/">davidschunk.com</a> ·
  <a href="https://everydayittips.com/">Everyday IT Tips</a> ·
  <a href="https://www.linkedin.com/in/dschunk/">LinkedIn</a>
</p>

<details>
<summary><strong>Personal-project boundary</strong></summary>

Unless a repository explicitly states otherwise, the work showcased here is maintained as independent personal, open-source, editorial, or community work. No affiliation with or endorsement by any current or former employer is implied. Public repositories are not intended to contain employer confidential or proprietary information, non-public internal configurations, customer data, credentials, or employer work product.

</details>
