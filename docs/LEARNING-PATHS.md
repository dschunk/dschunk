# Learning Paths

This guide is for people who want to use the repositories as a structured way to learn, not just as a collection of scripts.

The paths are intentionally practical. The goal is to understand **what evidence matters, why a tool asks for it, and what should happen before someone changes a production system**.

> Use labs, disposable VMs, test tenants, and sanitized data whenever possible. Do not learn by experimenting on production systems you do not fully understand.

## Path 1 — New to IT operations

**Goal:** learn how to observe a Windows system before changing it.

Start with:

1. [Everyday IT Tips — Windows Administration Hub](https://everydayittips.com/topics/windows/)
2. [SchunkOps Quick Start](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/QUICKSTART.md)
3. `Get-SchunkEndpointTriage`
4. `Test-SchunkDnsClient`
5. `Test-SchunkNetworkPath`
6. `Get-SchunkPendingReboot`

Learn to answer:

- Is the machine healthy enough to troubleshoot?
- Is the problem local, network, DNS, authentication, or service-related?
- What evidence belongs in a ticket?
- What should be captured before a reboot or configuration change?
- Which facts are observations, and which are assumptions?

**Suggested lab:** break DNS resolution on a disposable Windows VM, collect evidence, restore the configuration, and write a five-sentence incident summary.

## Path 2 — Help desk to systems administration

**Goal:** move from symptom collection to repeatable escalation.

Use:

- [Help Desk Field Guide](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/HELPDESK.md)
- `Get-SchunkEndpointTriage`
- `Get-SchunkDomainTrustStatus`
- `Get-SchunkEventTriage`
- `Get-SchunkServiceFailure`
- `Get-SchunkWindowsUpdateHealth`
- `Get-SchunkRdpHealth`

Practice:

- exporting structured evidence instead of screenshots;
- distinguishing endpoint failure from domain or network failure;
- writing an escalation that another technician can continue without repeating the first 20 minutes of troubleshooting;
- documenting what was checked, what was not checked, and why.

**Suggested lab:** create a mock ticket with an RDP failure. Collect enough evidence that a second student can diagnose the issue without access to the original machine.

## Path 3 — Windows Server and infrastructure

**Goal:** understand day-two operations, not just installation.

Use:

- [Senior Engineer Field Guide](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/SENIOR-ENGINEER.md)
- `Invoke-SchunkServerAudit`
- `Get-SchunkADReplicationHealth`
- `Get-SchunkGpoChangeAudit`
- `Get-SchunkDnsServerHealth`
- `Get-SchunkDhcpScopeHealth`
- `Get-SchunkCertificateInventory`
- `Get-SchunkDfsNamespaceHealth`
- `Get-SchunkWindowsBackupHealth`

Pair that with the operational templates in [Build It Like You Won't Be There Tomorrow](https://github.com/dschunk/build-it-like-you-wont-be-there).

**Suggested lab:** deploy a small Windows domain in a lab, document ownership/dependencies, run a health baseline, make one controlled change, and produce a handoff package.

## Path 4 — Active Directory, identity, and Group Policy

**Goal:** learn to troubleshoot identity as a distributed system.

Focus on:

- AD replication health
- machine trust
- account lockouts
- Kerberos / SPN ownership
- privileged-group review
- Group Policy application and change history
- DNS dependency

Start with:

```powershell
Get-SchunkADReplicationHealth
Get-SchunkAccountLockoutTrace -Identity jsmith -LookbackHours 24
Get-SchunkKerberosSpnAudit -Identity svc_web
Get-SchunkPrivilegedGroupAudit
Get-SchunkGpoChangeAudit -SinceDays 14 -IncludeFingerprint
```

**Suggested lab:** create a duplicate SPN in an isolated AD lab, observe the failure, identify ownership, and document the safe correction path without turning the diagnostic script into an automatic remediation tool.

## Path 5 — Microsoft 365 and Entra operations

**Goal:** establish facts before changing cloud identities or tenant configuration.

Start with:

- [SchunkOps Microsoft 365](https://github.com/dschunk/microsoft-365-ops)
- [Help Desk Guide](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/HELPDESK.md)
- [Operator Checklist](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/OPERATOR-CHECKLIST.md)
- [Senior Admin Guide](https://github.com/dschunk/microsoft-365-ops/blob/main/docs/SENIOR-ADMIN.md)

Learn to investigate:

- sign-in failures;
- license assignment;
- service-health incidents;
- mailbox forwarding and delegation;
- privileged users;
- guest lifecycle;
- Conditional Access;
- MFA registration;
- external Teams access.

**Suggested lab:** use a test tenant to build a user-support snapshot and explain which Graph permissions were required and why.

## Path 6 — Incident response and evidence

**Goal:** make before/after evidence part of remediation.

Use:

- [Incident Response Guide](https://github.com/dschunk/windows-it-toolkit/blob/main/docs/INCIDENT-RESPONSE.md)
- `New-SchunkIncidentBundle`
- `Compare-SchunkIncidentBundle`
- `Get-SchunkEventTriage`
- `Get-SchunkListeningPort`
- `Get-SchunkLogonFailure`

Practice:

1. capture before;
2. preserve timestamps and hashes;
3. make one controlled change;
4. capture after;
5. compare;
6. write the incident record.

**Suggested lab:** simulate a service outage, collect a full evidence bundle, remediate the service, collect a second bundle, and explain exactly what changed.

## Path 7 — Engineering leadership and operational maturity

**Goal:** evaluate whether a system is maintainable by a team rather than by one person.

Use:

- [Engineering Standards](ENGINEERING-STANDARDS.md)
- [System Runbook](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/system-runbook.md)
- [Engineering Handoff Checklist](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/handoff-checklist.md)
- [Disaster Recovery Plan](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/disaster-recovery-plan.md)
- [Backup and Restore Standard](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/backup-standard.md)
- [Post-Incident Review](https://github.com/dschunk/build-it-like-you-wont-be-there/blob/main/templates/post-incident-review.md)

Review a system by asking:

- Can someone else operate it?
- Is ownership clear?
- Are dependencies documented?
- Are failure modes visible?
- Is recovery tested?
- Are privileged actions auditable?
- Can changes be reversed?
- Is monitoring actionable?
- Does the documentation match reality?

## Recommended progression

A practical sequence is:

```text
Observe a single endpoint
        ↓
Collect repeatable evidence
        ↓
Understand identity + network dependencies
        ↓
Operate Windows Server roles
        ↓
Work across fleets / tenants
        ↓
Preserve incident evidence
        ↓
Design for handoff, recovery, and team ownership
```

Do not rush the progression. The point is not to memorize commands. The point is to learn how to ask better operational questions.
