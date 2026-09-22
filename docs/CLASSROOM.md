# Teaching & Classroom Guide

These repositories can be used as examples, lab material, discussion material, or starting points for assignments in IT, systems administration, cybersecurity, infrastructure, PowerShell, cloud administration, and technology-operations courses.

The strongest classroom use is not “run this script and get the answer.” It is:

> **What evidence does the tool collect, why does that evidence matter, what privileges are required, what could fail, and what should a responsible operator do next?**

## Suggested course modules

| Module | Level | Resource | Learning objective |
|---|---|---|---|
| Evidence-first troubleshooting | Intro | [SchunkOps Quick Start](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/QUICKSTART.md) | Separate observation from remediation and produce escalation-ready evidence |
| Windows endpoint triage | Intro / intermediate | `Get-SchunkEndpointTriage` | Read uptime, storage, networking, trust, reboot state, services, and event evidence as one support picture |
| DNS and network-path diagnosis | Intro / intermediate | `Test-SchunkDnsClient`, `Test-SchunkNetworkPath` | Distinguish name-resolution failures from transport failures |
| Active Directory health | Intermediate | `Get-SchunkADReplicationHealth` | Understand replication as a dependency for identity consistency |
| Kerberos and SPNs | Intermediate / advanced | `Get-SchunkKerberosSpnAudit` | Explain service identity, SPN ownership, and duplicate-registration failure modes |
| Group Policy evidence | Intermediate / advanced | `Get-SchunkGpoChangeAudit` | Treat policy as versioned operational state instead of a black box |
| Incident evidence | Intermediate / advanced | `New-SchunkIncidentBundle` | Preserve structured before/after evidence and integrity hashes |
| Microsoft 365 support | Intermediate | [M365 Help Desk Guide](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/HELPDESK.md) | Investigate identities, licensing, sign-ins, and mailbox context without immediately changing the tenant |
| Tenant security review | Advanced | [M365 Senior Admin](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/SENIOR-ADMIN.md) | Analyze privilege, mail flow, forwarding, delegation, guests, and service health |
| Operational documentation | Any | [Build It Like You Won't Be There Tomorrow](https://github.com/dschunk/build-it-like-you-wont-be-there) | Write runbooks, handoff plans, recovery plans, monitoring standards, and post-incident reviews |
| Operations interface design | Advanced | [Infrastructure Dashboard](https://github.com/dschunk/infrastructure-dashboard) | Discuss synthetic telemetry, status semantics, accessibility, audit history, and safe public demonstrations |

## A 50-minute class

**Topic:** “Collect first. Change second.”

1. **10 min — Scenario:** A user reports “the server is broken.”
2. **10 min — Evidence:** Review what endpoint/server triage should collect.
3. **15 min — Interpretation:** Students classify findings as fact, hypothesis, or missing evidence.
4. **10 min — Action plan:** Students propose the least disruptive next step.
5. **5 min — Handoff:** Each student writes a ticket update another technician could continue from.

Assessment can focus on reasoning rather than whether students guessed the final root cause.

## A two-hour lab

**Scenario:** Windows service outage in a disposable VM.

Students:

1. capture initial endpoint/server evidence;
2. inspect service state and recent events;
3. document a hypothesis;
4. make one controlled remediation;
5. collect a second evidence set;
6. compare before/after state;
7. produce a short incident record.

**Deliverables:**

- JSON or CSV evidence;
- command history;
- incident timeline;
- root-cause statement with confidence level;
- remediation;
- rollback path;
- one recommendation that would make the failure easier to detect next time.

## Capstone idea — Build for the next engineer

Ask students to deploy a small service and then grade the **handoff**, not only the service.

Required artifacts:

- architecture/dependency diagram;
- system runbook;
- access model;
- monitoring and alert definitions;
- backup and restore procedure;
- tested recovery notes;
- change plan;
- decommission checklist;
- known failure modes;
- operational owner and escalation path.

A different student or team should be able to operate the system using only the submitted artifacts.

## Discussion prompts

- Why is a read-only diagnostic tool often safer than an all-in-one remediation script?
- When does automation reduce risk, and when does it make failure faster?
- What belongs in structured output that does not belong in a screenshot?
- Why should backup success and restore success be treated as different claims?
- What makes an alert actionable?
- How should a script fail when a dependency or privilege is missing?
- Why are timestamps, hashes, and change records important during incidents?
- When is a public infrastructure demo useful, and what must be sanitized?
- What is the difference between “works on my machine” and operational readiness?
- How do you know documentation still describes the current system?

## Safe lab rules

For classroom use:

- use disposable VMs, sandboxes, lab domains, or test tenants;
- do not use production credentials or real customer/user data;
- sanitize hostnames, domains, IP addresses, usernames, tenant IDs, tokens, and incident evidence before submission;
- use least privilege and document required permissions;
- review scripts before execution;
- understand what a command reads or changes;
- do not publish secrets in GitHub issues, assignments, screenshots, or lab reports.

## Citation and attribution

Several flagship repositories include `CITATION.cff` files for formal citation. Instructors and students should use the citation metadata from the specific repository being referenced.

When adapting code or templates, follow the license in that repository and preserve required attribution.

## Instructor customization

These materials are intentionally modular. An instructor can:

- remove solution output and turn examples into troubleshooting exercises;
- provide broken lab states and ask students to collect evidence;
- require students to extend a script with validation or error handling;
- compare screenshot-based support with object-based evidence;
- ask advanced students to threat-model the tooling itself;
- use the operational templates as a peer-review rubric.

If a course uses these repositories, feedback through issues or pull requests is welcome when it improves clarity, safety, portability, or teaching value.
