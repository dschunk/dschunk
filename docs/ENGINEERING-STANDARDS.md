# Engineering Standards

This document describes the quality bar I try to apply across the core public engineering repositories.

It is not a claim that every project is perfect. It is a set of expectations that make the work easier to review, teach from, operate, and hand to somebody else.

## 1. Collect before changing

Diagnostics should establish state before remediation begins.

Why:

- evidence disappears after changes;
- multiple simultaneous changes destroy causal clarity;
- operators need a baseline;
- incident records are stronger when “before” and “after” are explicit.

Default preference: **read-only-first tooling**.

## 2. Structured output over screenshots

Where practical, operational tools should return objects that can be:

- read interactively;
- filtered and sorted;
- exported to JSON/CSV;
- archived;
- compared later;
- consumed by automation;
- tested.

A screenshot is useful for presentation. It is a weak data format.

## 3. Safe defaults

A tool should not surprise the operator.

Good defaults include:

- no hidden remediation;
- no destructive actions without explicit intent;
- least privilege;
- clear parameter names;
- bounded scope;
- useful error messages;
- validation before consequential operations;
- `ShouldProcess` / confirmation patterns when change actions are introduced.

## 4. Make privilege requirements visible

Documentation should state when a command requires:

- local administrator rights;
- domain privileges;
- RSAT;
- PowerShell remoting;
- Microsoft Graph scopes;
- Exchange Online roles;
- VMware PowerCLI;
- access to logs or remote systems.

Privilege should be a documented dependency, not a runtime surprise.

## 5. Explain failure behavior

Professional tooling needs to answer:

- What happens if the target is offline?
- What happens if a module is missing?
- What happens if one collector fails?
- Is partial output still returned?
- Is the failure distinguishable from “no findings”?
- Are timestamps and target identity preserved?

Unknown and failed are valid operational states. They should not silently become “healthy.”

## 6. Documentation is part of the system

A reusable project should make it possible to answer:

- what does this do?
- who is it for?
- how do I start?
- what permissions does it need?
- what does it not do?
- how do I test it?
- how does it fail?
- how do I contribute?
- how are security issues reported?
- how is it versioned?
- how should it be cited?

For production systems, add ownership, dependencies, monitoring, backup, recovery, change, and decommissioning.

## 7. Validation should be visible

Where the repository supports it, use automated validation for:

- syntax;
- linting;
- unit or repository tests;
- module import/export behavior;
- build output;
- broken references;
- deployment dry runs.

A passing badge is not proof that software is correct, but visible validation is better than an undocumented claim that “it works.”

## 8. Sanitize public examples

Public repositories should not contain:

- credentials or tokens;
- private keys;
- real customer data;
- private tenant identifiers;
- confidential host inventories;
- internal-only addresses;
- employer proprietary code or configurations;
- sensitive incident evidence.

Use synthetic or generic examples.

## 9. Separate demonstration from production

A public demo can show architecture, information design, workflow, and engineering reasoning without exposing real infrastructure.

Label synthetic telemetry as synthetic.  
Do not fake production authenticity by leaking production details.

## 10. Make handoff a design requirement

A system is not complete if the original builder must be present for normal operation.

A handoff-ready system has:

- a clear owner;
- documented dependencies;
- known failure modes;
- monitoring;
- recovery steps;
- access procedures;
- change history;
- escalation paths;
- decommission guidance.

The standard is not “can I run it?” It is **“can the next engineer understand and safely operate it?”**

## 11. Prefer small auditable tools over opaque mega-scripts

Focused tools are easier to:

- review;
- test;
- document;
- teach;
- reuse;
- troubleshoot;
- secure.

Composition is usually more maintainable than one script that discovers, decides, changes, restarts, and reports everything at once.

## 12. Treat recovery as a first-class feature

A backup is not evidence of recoverability.

Operational readiness should include:

- restore testing;
- rollback planning;
- evidence of last successful recovery test;
- defined recovery objectives where appropriate;
- documented dependencies required for restoration.

## Review questions for any project

Before calling a project mature, ask:

- Can a new user identify the intended audience in under a minute?
- Is there a safe quick start?
- Are dangerous assumptions documented?
- Can the output be preserved?
- Can a failure be distinguished from an empty result?
- Is the required access obvious?
- Is there a test or validation path?
- Is the security reporting path clear?
- Can another engineer maintain it?
- Can an instructor explain why the design choices matter?

These questions are the thread connecting the repositories in this profile.
