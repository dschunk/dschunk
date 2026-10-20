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
  <a href="https://www.davidschunk.com/hire">IT Consulting & Project Inquiries</a> ·
  <a href="https://www.davidschunk.com/writing">Writing & Reference</a> ·
  <a href="https://everydayittips.com/">Everyday IT Tips</a> ·
  <a href="https://www.linkedin.com/in/dschunk/">LinkedIn</a> ·
  <a href="https://meritpages.com/DavidSchunk">Academic & career record</a>
</p>

---

**[October 2026 portfolio website & GitHub maintenance review](docs/PORTFOLIO-AUDIT-2026-10-19.md)** — what shipped, production checks, and the remaining Voice of Adoptees deployment blocker.

## Find what you need

| If you are... | Start here | What you will find |
|---|---|---|
| **New to IT or PowerShell** | [Learning Paths](docs/LEARNING-PATHS.md) | Safe starting points, foundational concepts, guided labs, and a progression from first-line support to systems engineering |
| **Help desk / desktop support** | [SchunkOps Quick Start](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/QUICKSTART.md) | Endpoint triage, DNS, trust, RDP, SMB, reboot state, event evidence, and escalation-ready output |
| **Windows / infrastructure engineer** | [Windows IT Toolkit / SchunkOps](https://github.com/dschunk/windows-it-toolkit) | Read-only-first diagnostics for Windows Server, AD, GPO, Kerberos, DNS/DHCP, certificates, clusters, vSphere, and incident evidence |
| **Need a fast technical reference** | [IT Dictionary & Reference Library](https://everydayittips.com/dictionary/) | Practical definitions, ports, DNS records, PowerShell commands, AD troubleshooting commands, and Windows Server role references |
| **Microsoft 365 / Entra admin** | [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops) | Twenty read-only tools for identity, licensing, sign-ins, mailboxes, service health, Conditional Access, Teams, and security review |
| **Instructor / professor** | [Teaching & Classroom Guide](docs/CLASSROOM.md) | Assignment ideas, lab sequences, learning objectives, discussion prompts, and ways to use the repositories safely in class |
| **Engineering leader / architect** | [Engineering Standards](docs/ENGINEERING-STANDARDS.md) | Operational design principles, handoff expectations, evidence-first troubleshooting, recovery, change, and maintainability standards |
| **Need Windows Server or Active Directory help?** | [Independent IT consulting](https://www.davidschunk.com/hire) | Discuss Windows Server, identity, PowerShell automation, troubleshooting, infrastructure and operational documentation projects, subject to availability and applicable approvals |
| **Looking for the whole portfolio** | [Repository Map](docs/REPOSITORY-MAP.md) | A curated index of technical, writing, research, community, and case-study projects |

> **Operating principle:** Collect evidence first. Make the fix repeatable. Leave the next engineer a map.

### Quick portfolio tour

| Explore | What you can use today |
|---|---|
| **[SchunkOps for Windows](https://github.com/dschunk/windows-it-toolkit)** | A PowerShell toolkit for Windows and Active Directory operations, triage and incident evidence |
| **[SchunkOps for Microsoft 365](https://github.com/dschunk/microsoft-365-ops)** | Read-only-first Entra, Exchange Online and Microsoft 365 operational diagnostics |
| **[Everyday IT Tips](https://everydayittips.com/)** | Published field guides, a searchable technical dictionary and practical reference material |
| **[Professional portfolio](https://www.davidschunk.com/)** | Selected projects, independent writing, background and contact information |

## Fresh from the workbench

- **[Download TicketReady — Free Windows Support Report (ZIP)](https://github.com/dschunk/windows-it-toolkit/releases/download/ticketready-v0.2.2/TicketReady-v0.2.2.zip)** — free portable Windows support tool with guided troubleshooting, private HTML/JSON reports and before/after comparisons; no installation or upload. [Source & privacy notes](https://github.com/dschunk/windows-it-toolkit/tree/main/tools/TicketReady).
- **[Microsoft Entra Connect sync troubleshooting](https://everydayittips.com/guides/entra-connect-sync-error-troubleshooting/)** — trace scheduler state, connector operations, and object-level errors before forcing synchronization.
- **[Exchange Online shared mailbox access audit](https://everydayittips.com/guides/exchange-online-shared-mailbox-audit/)** — verify Full Access, Send As, Send on Behalf, and forwarding without changing tenant permissions.
- **[Windows DNS dynamic registration and stale records](https://everydayittips.com/guides/windows-dns-dynamic-registration-troubleshooting/)** — correlate DNS responses, client configuration, DHCP evidence, and record ownership.
- **[Troubleshoot Slow Windows Domain Logons and Group Policy Processing](https://everydayittips.com/guides/windows-slow-domain-logon-gpo-diagnostics/)** — correlate Group Policy events, domain controller discovery and profile evidence before changing a production workstation.
- **[Troubleshoot Windows TLS Certificate Chain and Revocation Errors](https://everydayittips.com/guides/windows-tls-certificate-chain-troubleshooting/)** — investigate chain trust, AIA/CDP retrieval, hostname issues and relying-application context without bypassing validation.
- [AI Is an Operating Model, Not a Purchase Order](https://www.davidschunk.com/writing/enterprise-ai-strategy) — an independent 180-day plan for enterprise AI governance, adoption, security, and measurable outcomes across departments.
- [Enterprise AI pilot checklist](https://everydayittips.com/guides/enterprise-ai-pilot-checklist/) — scope, secure, evaluate, and support a real AI workflow.
- [AI connector security and prompt injection](https://everydayittips.com/guides/ai-prompt-injection-connector-security/) — access boundaries, adversarial tests, approvals, and operational monitoring.
- [Active Directory time sync and Kerberos clock skew](https://everydayittips.com/guides/active-directory-time-sync-kerberos/) — inspect the Windows Time hierarchy and establish evidence before changing clocks.
- [Windows scheduled-task failure triage](https://everydayittips.com/guides/windows-scheduled-task-failure-triage/) — investigate execution identities, task history, working directories, and actual job outcomes.
- [Between Russia and Ukraine: A Case for Peace with Guarantees](https://www.davidschunk.com/writing/between-russia-and-ukraine) — independent personal essay on heritage, diplomacy, Ukrainian sovereignty, and European security.

## How these projects are built

The work here follows a consistent standard: **read-only-first tooling**, inspectable output, reproducible field guides, operational verification, and handoff documentation. Examples use generic lab data, not employer or customer systems.

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

### Everyday IT Tips Reference Library

A growing professional reference library for administrators, engineers, support staff, students, and instructors.

- [IT Dictionary](https://everydayittips.com/dictionary/) — practical definitions with operational context
- [Common ports and protocols](https://everydayittips.com/guides/common-ports-protocols-reference/) — TCP/UDP reference with troubleshooting notes
- [PowerShell command reference](https://everydayittips.com/guides/powershell-windows-admin-command-reference/) — Windows administration by troubleshooting question
- [Active Directory troubleshooting commands](https://everydayittips.com/guides/active-directory-troubleshooting-command-reference/) — dcdiag, repadmin, nltest, gpresult, klist, w32tm, and AD PowerShell
- [DNS record types](https://everydayittips.com/guides/dns-record-types-reference/) — A, AAAA, CNAME, MX, TXT, SRV, PTR, NS, SOA, CAA, and verification
- [Windows Server roles and features](https://everydayittips.com/guides/windows-server-roles-features-reference/) — role purpose, dependencies, inventory, and validation

The full writing and research index also lives at [davidschunk.com/writing](https://www.davidschunk.com/writing).

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

- [IT Dictionary](https://everydayittips.com/dictionary/)
- [Common ports and protocols IT professionals should know](https://everydayittips.com/guides/common-ports-protocols-reference/)
- [PowerShell command reference for Windows administrators](https://everydayittips.com/guides/powershell-windows-admin-command-reference/)
- [Active Directory troubleshooting command reference](https://everydayittips.com/guides/active-directory-troubleshooting-command-reference/)
- [DNS record types IT professionals should know](https://everydayittips.com/guides/dns-record-types-reference/)
- [Before you reboot a Windows Server, capture this first](https://everydayittips.com/articles/before-you-reboot-capture-evidence/)

## Research

### [Checks and Balances for Artificial Intelligence](https://www.davidschunk.com/research/ai-governance)

A risk-tiered governance framework focused on human agency, accountability, evidence, deployment controls, independent review, and stronger safeguards as capability and consequence increase.

[Canonical paper](https://www.davidschunk.com/research/ai-governance) · [Source-controlled copy](research/checks-and-balances-for-artificial-intelligence.md)

## Selected web projects

These are smaller than the core engineering repositories, but they show the other side of the work: product thinking, deployment, UI, public-facing operations, and maintaining real sites.

- [Department of Cash](https://departmentofcash.com/) — a practical personal-finance interface focused on recurring bills, cash flow, and making everyday money management easier to understand.
- [DoTheyPass](https://dotheypass.com/) — a privacy-conscious public-source identity-consistency project with explicit uncertainty, provenance, and safety controls.
- [BHS 2013](https://bhs2013.com/) — an alumni portal project for the Bedford High School Class of 2013.
- [DavidSchunk.com](https://www.davidschunk.com/) — personal publishing, research, technical writing, project index, and collaboration hub.


## Community work

Technology is not the only thing I work on.

- [Voice of Adoptees](https://voiceofadoptees.com/) — long-form conversations centered on adoptee voices and lived experience.
- [Russian Adoptees Organization](https://russianadoptees.com/) — community resources and infrastructure for adoptees from Russia and the former Soviet Union.

## About

I'm David Schunk, a Senior IT Engineer and Champlain College Class of 2017 graduate based in New Hampshire. My work spans Windows infrastructure, systems administration, automation, networking, virtualization, cloud technologies, Microsoft 365, identity, and cybersecurity.

I care about a specific kind of engineering: **systems that are understandable under pressure, recoverable after failure, and maintainable by someone other than the person who built them.**

That same idea drives the tools, documentation, field guides, reference library, research, and operational templates in this profile.

<p align="center">
  <a href="https://www.davidschunk.com/">davidschunk.com</a> ·
  <a href="https://everydayittips.com/">Everyday IT Tips</a> ·
  <a href="https://www.linkedin.com/in/dschunk/">LinkedIn</a>
</p>

<details>
<summary><strong>Personal-project boundary</strong></summary>

Unless a repository explicitly states otherwise, the work showcased here is maintained as independent personal, open-source, editorial, or community work. No affiliation with or endorsement by any current or former employer is implied. Public repositories are not intended to contain employer confidential or proprietary information, non-public internal configurations, customer data, credentials, or employer work product.

</details>
