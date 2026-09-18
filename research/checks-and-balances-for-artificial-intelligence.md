# Checks and Balances for Artificial Intelligence

## A Risk-Tiered Framework for Safety, Accountability, Public Trust, and Innovation

**David Schunk**  
Version 1.0 · September 18, 2026  
Independent research and policy analysis

> **Central proposition:** Artificial intelligence does not need to be made harmless to be governable. It needs to be observable, constrained, testable, contestable, and recoverable. Increasing capability should produce increasing evidence, increasing controls, and increasing accountability.

Canonical publication: https://www.davidschunk.com/research/ai-governance

---

## Abstract

The central problem in artificial-intelligence governance is not whether society should choose innovation or safety. It is whether powerful systems can be deployed while preserving human agency, accountability, security, competition, and the ability to correct failure.

Public anxiety about AI is often answered with reassurance: the technology will improve, companies are testing their systems, regulators are paying attention, and people will adapt. Those statements may be sincere, but reassurance is not a control. Mature engineering disciplines reduce risk through defined responsibilities, independent evidence, incident learning, access controls, redundancy, recovery procedures, and consequences when obligations are ignored.

This paper proposes a risk-tiered governance model. Ordinary low-impact AI should face lightweight baseline duties. Systems that materially influence employment, credit, education, housing, insurance, health, essential services, or legal rights should face stronger assessment, documentation, human-review, and appeal requirements. Frontier systems that cross defined capability thresholds associated with plausible severe or large-scale harm should face capability evaluations, deployment gates, security controls, incident reporting, external testing, and independent review.

The institutional design is deliberately plural. Legislatures define rights and accountability. Technical standards bodies define measurement methods. Sector regulators enforce obligations in context. Independent evaluators test consequential claims. Courts preserve due process and redress. Scientific bodies update the evidence base. Companies remain responsible for engineering and operating their systems. No single institution receives unlimited authority, and no developer is permitted to grade its own homework as the sole proof of safety.

The framework can be summarized as four layers:

1. **Rights at the user layer.**
2. **Controls at the deployment layer.**
3. **Evidence at the audit layer.**
4. **Emergency brakes at the frontier layer.**

---

## 1. Govern AI like consequential infrastructure

The phrase "regulate AI" is too broad to be useful. A spam filter, a hospital triage model, an autonomous coding agent, a hiring system, and a frontier general-purpose model are all called AI, yet their plausible harms, affected populations, reversibility, and scale are radically different.

Rules based only on whether software uses machine learning will either overregulate ordinary tools or underregulate systems with genuine capacity for widespread harm.

A better objective is **governability**.

A governable system has:

- an identifiable owner;
- documented intended uses and limits;
- controlled access to consequential capabilities;
- logs sufficient to reconstruct important events;
- tests tied to real failure modes;
- escalation procedures;
- recovery and rollback procedures;
- a meaningful appeal path when people are materially affected; and
- an accountable organization that cannot escape responsibility by blaming "the algorithm."

The goal is not zero risk. No serious technology operates at zero risk.

The goal is that increasing power produces increasing evidence, controls, and accountability.

A durable governance system should therefore evaluate at least four factors:

**Capability.** What can the model or system actually do?

**Consequence.** What is the severity of a plausible failure or misuse?

**Exposure.** How many people, systems, institutions, or critical functions could be affected?

**Reversibility.** Can a bad outcome be detected, stopped, corrected, and repaired?

The same model can move between risk categories depending on deployment. A model used to summarize internal meeting notes may be low impact. The same model connected to production credentials and authorized to make irreversible infrastructure changes has a very different risk profile.

Governance must follow the deployed system, not merely the model artifact.

---

## 2. Public trust is an engineering problem

Public anxiety about AI should not be dismissed as ignorance.

Pew Research Center reported in June 2026 that roughly seven in ten Americans expected AI to make personal information less secure. Sixty-seven percent reported little or no confidence in the federal government to regulate AI effectively, and roughly six in ten lacked confidence that U.S. companies would develop and use AI responsibly.

Stanford's 2026 AI Index similarly describes a public that can see potential benefits while remaining nervous about AI.

That combination is rational.

People routinely accept high-powered technologies when the rules around them are legible. Passengers do not personally inspect aircraft engines. They rely on an institutional safety system built from certification, maintenance, incident investigation, crew qualification, operating rules, redundancy, and legal responsibility.

Those controls do not eliminate crashes. They make risk measurable, responsibility assignable, and improvement cumulative.

AI needs an equivalent social contract.

A person should not have to understand transformer architectures to know whether an automated decision affected a job application. A parent should not need to reverse engineer a chatbot to know whether a product marketed to minors has safety controls. A company buying an AI service should not have to rely solely on a vendor's assertion that the model is "enterprise secure."

Public confidence can grow when people know:

- when AI is being used;
- who owns the decision;
- what the system was tested for;
- who verified consequential claims;
- how incidents are reported;
- what controls exist;
- how a person can appeal; and
- what happens when the system fails.

"Trust us" is a public-relations statement.

"Here is the test, the result, the independent reviewer, the incident process, and your appeal right" is governance.

---

## 3. Regulate risk, not the label

Current standards and laws already point toward a risk-based approach.

The U.S. National Institute of Standards and Technology's AI Risk Management Framework is voluntary and lifecycle-oriented. It emphasizes characteristics including validity and reliability, safety, security and resilience, accountability and transparency, explainability and interpretability, privacy, and fairness.

The European Union AI Act uses risk categories and establishes specific obligations for high-risk systems and general-purpose AI models with systemic risk.

ISO/IEC 42001 establishes an AI management-system framework. ISO/IEC 23894 provides AI-specific risk-management guidance.

The OECD AI principles emphasize robustness, security, safety, traceability, transparency, and systematic risk management.

These approaches differ significantly in legal force, philosophy, and institutional design. They nevertheless share an important premise: AI risk is contextual.

A useful classification should examine:

1. the decision or action the system performs;
2. the severity of plausible harm;
3. the number and vulnerability of people exposed;
4. the system's autonomy and access to tools;
5. the difficulty of detecting or reversing an error; and
6. the underlying capabilities of the model or system.

Classification must also remain dynamic. A system should be reclassified when new capabilities, integrations, permissions, or deployment contexts materially change its risk.

---

## 4. Three tiers of obligation

### Tier 1 — Ordinary or limited-impact AI

Examples include drafting aids, search assistance, low-stakes recommendations, spam filtering, translation, summarization, and internal productivity tools that lack consequential authority.

Baseline obligations should be light enough that ordinary software development remains practical:

- truthful disclosure where an artificial interaction could reasonably be mistaken for a human;
- reasonable privacy and security protections;
- a documented system owner;
- a documented intended use;
- basic logging for material automated actions; and
- prohibitions on deceptive representations about capabilities or guarantees.

This tier should not require expensive licensing or recurring independent audits simply because a product uses machine learning.

### Tier 2 — High-impact or consequential AI

This tier includes systems that materially influence employment, credit, education, housing, insurance, health, essential services, legal rights, or similarly consequential outcomes.

Additional requirements should include:

- a documented impact assessment;
- data and performance documentation;
- testing relevant to the affected population and deployment context;
- subgroup or disparity testing where relevant and lawful;
- human review with actual authority;
- notice to affected people;
- a meaningful appeal path;
- records sufficient to reconstruct the decision;
- change-management procedures;
- post-deployment monitoring; and
- independent evaluation proportionate to the risk.

The key concept is consequence. A system can be technologically ordinary and still be high impact if it decides something important about a person's life.

### Tier 3 — Frontier-capability or systemic-risk AI

This tier should be triggered by defined capabilities associated with plausible severe or large-scale harm.

Possible categories include advanced cyber capabilities, biological or chemical enablement, dangerous autonomous behavior, large-scale manipulation, model self-improvement or replication capabilities, or other evidence-backed thresholds that materially increase systemic risk.

Additional requirements should include:

- a structured safety case;
- adversarial capability evaluation;
- red-team testing;
- threat modeling;
- staged deployment;
- strong model-weight, credential, and infrastructure security;
- incident reporting;
- independent external evaluation;
- protected internal escalation;
- executive accountability;
- predefined deployment-restriction or rollback triggers; and
- tested emergency intervention procedures.

Thresholds should not rely only on training compute. Compute can be an indicator, but algorithmic progress can make a fixed threshold obsolete. Capability tests, deployment context, access level, and demonstrated dangerous functionality should all matter.

Legislation can define the duty to evaluate and control risk. Technical standards can update measurement methods more frequently than statutes.

---

## 5. Rights at the user layer

When AI materially affects a person, four rights should travel with the decision.

### Right to know

People should receive clear notice when an automated system materially participates in a consequential decision or when they are interacting with an artificial agent in a context where human identity matters.

The disclosure should be understandable. Burying "AI may be used" in a twenty-page terms-of-service document is not meaningful notice.

### Right to an intelligible reason

A person should be able to understand the material basis of a consequential outcome.

This does not require publication of proprietary source code, model weights, or every mathematical parameter. It does require enough information to understand the relevant factors, data categories, policy basis, and decision process.

### Right to contest

A consequential automated outcome should have a meaningful review process.

People should be able to correct materially inaccurate data and reach a human reviewer who has sufficient information, time, training, and authority to change the outcome.

A human who automatically clicks "approve" is not meaningful human oversight.

### Right to accountable ownership

Organizations should remain responsible for systems they deploy.

"The model did it" must not become a liability sink. If an organization delegates a consequential function to AI, it retains the obligation to control, monitor, and answer for that function.

These rights reduce fear because they preserve human agency.

---

## 6. Controls at the deployment layer

Many serious AI failures will not come from an abstract model suddenly becoming malicious.

They will come from ordinary systems-engineering failures:

- excessive permissions;
- weak authentication;
- secrets in prompts or logs;
- unreviewed automation;
- poor change control;
- brittle integrations;
- unsafe defaults;
- missing monitoring;
- ambiguous ownership; and
- no recovery plan.

AI deployments should therefore inherit mature infrastructure and security controls.

### Least privilege

An AI system should receive no more authority than required for the task.

Agents should use dedicated identities rather than shared administrator credentials. Tool access should be granular. High-risk privileges should be separately granted.

### Segmentation

Development, test, and production environments should be separated. AI systems should not be able to move freely between data stores, networks, identity domains, or administrative planes without an explicit policy reason.

### Deterministic policy gates

High-risk actions should not depend solely on a probabilistic model deciding whether its own action is safe.

Organizations should use deterministic checks for defined constraints: transaction ceilings, allowlists, approval requirements, data-loss-prevention rules, environment boundaries, and other hard controls.

### Human approval where consequence justifies it

Human authorization is valuable when it is real.

Actions such as deleting production data, changing privileged access, executing high-value transactions, releasing sensitive information, or modifying critical infrastructure can require human approval even when the AI agent performs the preparatory work.

### Rate limits and exposure limits

A small mistake becomes a large incident when automation can repeat it at machine speed.

Rate limits, spend limits, transaction limits, concurrency caps, and bounded action windows can reduce blast radius.

### Logging and evidence

Material actions should create durable evidence: who or what initiated the action, which model or version was involved, what tools were invoked, what policy checks ran, what approvals occurred, and what changed.

### Change control and staged rollout

New models, prompts, tools, permissions, and safety policies should be treated as changes to production systems.

Canary deployments, limited cohorts, rollback plans, predeployment testing, and post-change monitoring matter.

### Recovery

A system that cannot be recovered safely should not receive irreversible authority.

Backups, rollback, credential revocation, service isolation, and incident runbooks should be designed before failure.

**Operational rule: an AI system should never receive more authority than the organization can monitor, explain, and recover from.**

---

## 7. Evidence at the audit layer

Transparency alone is not accountability.

A model card may be accurate or incomplete. An internal benchmark may be rigorous or optimized. A policy may exist on paper while operational practice differs substantially.

The U.S. National Telecommunications and Information Administration has described an AI accountability chain involving information, independent evaluation, and consequences. That is a useful model.

Important claims should map to measurable tests.

Examples:

- Does the system meet the reliability threshold its vendor advertises?
- Does a high-impact classifier produce materially different error rates across relevant populations?
- Can an agent exceed its assigned permissions?
- Does a safeguard remain effective under adversarial prompting?
- Can a security claim be reproduced by an evaluator using sequestered test data?
- Can a system be rolled back under simulated incident conditions?
- Are the logs sufficient to reconstruct a consequential automated action?

Independent evaluation should be proportional to risk. There is no reason to require a third-party audit for every autocomplete feature. There is a strong reason not to let a developer be the sole verifier of a claim that a frontier system cannot perform a dangerous capability.

NIST's 2026 Artificial Intelligence Technology Evaluation program and TEVV-Athlon work are important because they push toward objective and repeatable evaluation. Sequestered or blind tests can reduce contamination and gaming.

Auditors need checks and balances too.

Accreditation criteria, conflict-of-interest rules, methodological transparency, quality review, regulator access to work papers, and consequences for negligent certification are necessary to prevent the audit market from becoming a race for favorable badges.

The standard should not be "an audit happened."

The standard should be "a consequential claim was tested competently, the evidence was retained, and failure triggers a defined response."

---

## 8. Emergency brakes at the frontier layer

Public debate often asks whether advanced AI should have a "kill switch."

The phrase is too simple for real systems.

Modern AI services may include distributed model serving, APIs, user accounts, autonomous agents, tools, credentials, caches, customer deployments, local copies, and potentially downloadable weights.

The useful question is not whether a red button exists.

The useful question is whether operators have tested intervention capabilities.

Those can include:

- suspending new accounts;
- rate-limiting dangerous functionality;
- revoking credentials;
- isolating tools;
- disabling a specific high-risk feature;
- rolling back a model version;
- restricting model-weight access;
- pausing a deployment stage;
- preserving incident evidence; and
- shutting down affected serving infrastructure when necessary and technically possible.

These controls should be assigned to named roles, tested before an emergency, protected against unauthorized use, and included in incident exercises.

### Safety cases

Before a system crosses a defined frontier threshold, the developer should produce a structured **safety case**.

A safety case should answer:

- What dangerous capabilities were tested?
- What threats were considered?
- What did adversarial testing find?
- What mitigations were implemented?
- What residual risks remain?
- What security protects model weights and privileged access?
- What monitoring exists after deployment?
- What incident thresholds trigger escalation?
- What conditions trigger deployment restriction or rollback?
- Who can challenge the evidence?

A safety case should be an evidence-backed argument, not a marketing document.

OpenAI's Preparedness and Frontier Governance frameworks, Anthropic's Responsible Scaling Policy, and Google DeepMind's Frontier Safety Framework use versions of capability-triggered controls. These are company-authored frameworks and should not be treated as independent proof of safety. They are nevertheless evidence that capability-linked governance is operationally feasible and can inform public standards.

---

## 9. Institutional checks and balances

AI is too broad for one agency, one standards body, one laboratory, or one company to control competently.

Authority should be distributed.

### Legislatures

Define rights, scope, liability, enforcement authority, appropriations, and the democratic boundaries of regulation.

### Technical standards bodies

Maintain terminology, test methods, risk-management profiles, measurement protocols, and interoperability standards.

### Sector regulators

Apply obligations within the context of finance, health, employment, communications, transportation, critical infrastructure, and other regulated domains.

### Independent evaluators

Test consequential claims, reproduce results, run red-team exercises, and challenge developer evidence.

### Courts

Preserve due process, review government action, adjudicate liability, and provide remedies.

### Independent scientific bodies

Update the evidence base and advise on emerging capabilities without unilaterally writing criminal or civil rules.

### Companies and deployers

Remain responsible for engineering, security, documentation, monitoring, incident response, and truthful representations.

### The public and civil society

Receive usable transparency, report harms, scrutinize policy, participate in rulemaking, and challenge institutions.

This redundancy is defense in depth.

A regulator can become stale or captured. A company can grade its own homework. An auditor can become economically dependent on clients. A standards body can become detached from democratic accountability. Courts can move slowly.

Multiple independent checks reduce the chance that one institutional failure becomes the only failure that matters.

International coordination should focus on interoperable evidence rather than requiring identical law.

The Council of Europe's AI Framework Convention, OECD principles, EU AI Act, UN Global Digital Compact, and national systems reflect different legal traditions. They do not need to merge into one global AI regulator.

They can converge on common artifacts:

- risk assessments;
- evaluation reports;
- incident taxonomies;
- audit evidence;
- provenance standards;
- safety cases; and
- security controls.

---

## 10. Incident reporting and learning

Cybersecurity matured partly through shared concepts of vulnerabilities, indicators, severity, coordinated disclosure, post-incident review, and response.

AI needs an analogous incident culture.

A serious AI incident could include:

- unauthorized acquisition of frontier model weights;
- demonstrated bypass of safeguards that enables severe harm;
- a consequential automated system producing widespread unlawful outcomes;
- an agent causing material unauthorized transactions;
- exploitation of an AI integration to access protected data; or
- discovery of a capability that materially changes the system's risk classification.

Reports should separate confidential technical details from public learning.

Regulators may need sensitive exploit details or architecture that should not be posted immediately. The public still deserves timely information about the nature of significant incidents, affected groups, corrective actions, and systemic lessons.

A two-layer disclosure model can protect security without making secrecy the default.

Whistleblower protection is also a safety control.

People inside an organization may see ignored test failures, manipulated metrics, security gaps, or pressure to deploy before outsiders do. Protected escalation channels reduce the chance that commercial incentives suppress material safety information.

---

## 11. Synthetic media and provenance

Detection tools will remain useful, but attempting to classify every image, recording, or document as "AI-generated" is fragile.

As generation improves, detection can fail. Ordinary editing complicates binary labels. False accusations can be damaging.

Provenance provides a complementary strategy.

Standards such as C2PA allow content to carry cryptographically verifiable information about origin and transformation. NIST has also evaluated provenance, watermarking, authentication, and synthetic-content detection.

Policy should encourage interoperable provenance where authenticity matters while recognizing the limitations:

- metadata can be stripped;
- legacy content will lack credentials;
- not every camera or editor will participate;
- absence of provenance is not evidence of deception; and
- credentials themselves require secure issuance and verification.

Disclosure should also be context-sensitive.

Labeling every spell-check or background cleanup creates warning fatigue. Disclosure matters most where identity, authenticity, public persuasion, or consequential decision-making is at stake.

---

## 12. Innovation, open models, and competition

Overregulation can create safety problems of its own.

A compliance regime with fixed multimillion-dollar burdens can entrench incumbents, discourage open research, and push experimentation into less visible environments.

A risk-tiered framework should therefore:

- keep Tier 1 obligations inexpensive;
- provide sandboxes for novel deployments;
- publish open test methods;
- provide templates and reference controls for smaller organizations;
- scale fees and audit depth to consequence and capability;
- preserve legitimate research; and
- avoid making safety compliance synonymous with dependence on a handful of large vendors.

Open models require nuance.

Openly available weights can support research, competition, reproducibility, local control, and resilience against vendor lock-in. They can also make some safety controls difficult to enforce after release.

"Open" should not be treated as inherently safe or inherently dangerous.

Obligations should turn on:

- demonstrated capability;
- foreseeable severity of misuse;
- whether the release materially changes access to dangerous capability;
- the degree of downstream control retained by the distributor; and
- the feasibility of meaningful mitigation.

Procurement can also promote competition.

Governments and large enterprises should demand exportable logs, documented interfaces, clear data-ownership terms, access to necessary audit evidence, and realistic vendor-exit plans.

The United States' current federal framework emphasizes innovation, competition, infrastructure, national security, child safety, intellectual property, free speech, workforce issues, and greater national uniformity. The European Union has adopted a more prescriptive statutory risk framework.

Reasonable policymakers can disagree about the balance.

The proposal here can operate under either philosophy because it separates public obligations from fast-changing technical measurement methods.

---

## 13. Implementation roadmap

### Phase I — Common language and baseline controls (0–12 months)

- Adopt a common taxonomy for ordinary, high-impact, and frontier-capability systems.
- Define consequential domains.
- Establish minimum user notice, appeal, and evidence-retention rights.
- Create standardized AI incident categories and protected reporting channels.
- Publish baseline security controls for agents and AI services.
- Fund open evaluation tooling and sequestered public-interest testbeds.
- Require government procurement to collect risk, testing, incident, and exit-plan evidence.

### Phase II — Independent assurance (12–24 months)

- Accredit AI evaluation organizations.
- Define conflict-of-interest and audit-quality standards.
- Require independent testing for specified high-impact systems and frontier thresholds.
- Create protected researcher access and vulnerability-disclosure processes.
- Publish anonymized incident trends and corrective-action lessons.
- Evaluate whether requirements are imposing disproportionate burdens on small organizations.

### Phase III — Frontier gates and international interoperability (24–60 months)

- Maintain capability thresholds through technical rulemaking informed by independent science.
- Require safety cases before specified frontier deployment thresholds are crossed.
- Mutually recognize compatible evaluation artifacts across jurisdictions where standards are equivalent.
- Run recurring cross-border exercises for cyber, biosecurity, model theft, and large-scale service incidents.
- Review rules on a fixed cycle so obsolete obligations are revised or expire rather than accumulating indefinitely.

Measurement should come first.

Governments cannot reliably enforce a safety requirement that no one knows how to test. When measurement is immature, policy should require transparent risk management, evidence retention, incident reporting, and research investment rather than inventing false precision.

---

## 14. Counterarguments and failure modes

A credible governance proposal must explain how it can fail.

### Risk tiers can become a compliance game

Organizations may classify systems downward or optimize specifically for threshold tests.

Mitigations include multiple classification indicators, post-deployment evidence, regulator authority to reclassify systems, random or sequestered tests, and penalties for materially false representations.

### Independent audits can become rubber stamps

Correct.

Financial and security auditing show that independence on paper is insufficient. Accreditation, methodology review, conflict rules, regulator inspection, reproducibility, and consequences for negligent certification are necessary.

### Transparency can create security risks

Correct.

Publishing sensitive prompts, exploit details, exact defenses, privileged architecture, or model weights may help attackers.

Transparency should mean that regulators and the public receive enough evidence to establish accountability, not that every security-sensitive artifact is posted online.

Confidential regulator access and public summaries can coexist.

### Human review can become theater

A human who has seconds to approve an algorithmic recommendation, lacks context, or cannot change the outcome is not meaningful oversight.

Meaningful review requires time, information, authority, and training.

In some systems, constraining the AI's authority is more effective than inserting a symbolic human click.

### Rules can freeze today's technology

This is why legislation should define rights, duties, and governance outcomes while technical standards define test methods that can update more frequently.

Scheduled review should force policymakers to revisit assumptions.

### No framework eliminates catastrophic risk

True.

No cybersecurity framework eliminates breaches, no aviation regime eliminates crashes, and no financial regulation eliminates fraud.

Governance should be judged by whether it reduces expected harm, increases detection, improves recovery, creates accountability, and produces learning.

### Who decides what risk is acceptable?

Ultimately, democratic institutions must set legal boundaries.

Engineers and scientists can measure capabilities, reliability, exposure, and control effectiveness. They cannot unilaterally decide how society should trade liberty, privacy, safety, innovation, competition, and national security.

That division of authority is a feature of checks and balances.

---

## 15. What the public should be able to expect

A mature AI governance system should eventually be explainable without legal training.

People should be able to expect that:

- an organization cannot secretly use AI to make a consequential decision and then deny that automation mattered;
- a person can challenge a consequential automated outcome;
- a real human with authority can correct a high-impact error;
- companies remain responsible for systems they deploy;
- powerful AI connected to real systems receives permissions no broader than necessary;
- high-impact claims are backed by tests;
- the most consequential claims are not verified only by the seller;
- serious incidents are reported, investigated, and used to improve controls;
- frontier systems face stronger safeguards as dangerous capabilities increase;
- safety rules do not make ordinary low-risk software prohibitively expensive to build;
- government oversight remains reviewable through law, courts, public rulemaking, and transparent standards; and
- no one is asked to accept "AI said so" as the end of the conversation.

This is a more durable public compact than promising that AI will be benevolent.

It accepts that software, companies, regulators, auditors, and people all make mistakes.

The system is designed around that fact.

---

## Conclusion

Artificial intelligence is moving from a tool people query to infrastructure that can perceive, recommend, decide, generate, communicate, and increasingly act.

That transition deserves serious governance.

Serious does not have to mean fearful, centralized, or hostile to innovation.

The most durable path is familiar to anyone who has operated consequential technology:

- understand the system;
- limit its authority;
- test it before trusting it;
- preserve evidence;
- monitor it in production;
- plan for failure;
- make recovery possible;
- assign ownership; and
- bring in an independent set of eyes when the stakes justify it.

Public fear will not disappear because experts insist that a model is safe.

It can diminish when people see institutions capable of saying **no**, systems designed to stop at defined boundaries, auditors capable of challenging claims, courts capable of providing remedies, engineers capable of recovering from failure, and laws that preserve human agency.

> **AI should be powerful enough to be useful and governed enough to remain accountable to people.**

The task is not to build one perfect regulator or one perfect model.

It is to build a layered system in which no single failure — technical, commercial, institutional, or human — has to become a catastrophe.

That is what checks and balances are for.

---

## Selected sources and authorities

1. National Institute of Standards and Technology, **Artificial Intelligence Risk Management Framework (AI RMF 1.0)** — https://www.nist.gov/itl/ai-risk-management-framework
2. NIST, **Generative Artificial Intelligence Profile (NIST AI 600-1)** — https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence
3. NIST, **Artificial Intelligence Technology Evaluation (AITE)** — https://www.nist.gov/news-events/news/2026/07/announcing-nists-artificial-intelligence-technology-evaluation-aite
4. NIST, **TEVV-Athlon Framework for Evaluating AI Systems** — https://www.nist.gov/artificial-intelligence/ai-research/tevv-athlon-framework-evaluating-ai-systems
5. National Telecommunications and Information Administration, **AI Accountability Policy Report** — https://www.ntia.gov/issues/artificial-intelligence/ai-accountability-policy-report
6. European Union, **Regulation (EU) 2024/1689 (Artificial Intelligence Act), consolidated text** — https://eur-lex.europa.eu/eli/reg/2024/1689/2026-07-27/eng
7. ISO/IEC 42001:2023, **Artificial intelligence management system** — https://www.iso.org/standard/42001
8. ISO/IEC 23894:2023, **Guidance on risk management for AI** — https://www.iso.org/standard/77304.html
9. OECD, **Recommendation of the Council on Artificial Intelligence** — https://legalinstruments.oecd.org/en/instruments/OECD-LEGAL-0449
10. Council of Europe, **Framework Convention on Artificial Intelligence and Human Rights, Democracy and the Rule of Law** — https://www.coe.int/en/web/artificial-intelligence/the-framework-convention-on-artificial-intelligence
11. United Nations, **Global Digital Compact** — https://www.un.org/pact-for-the-future/en/annex-i-global-digital-compact
12. United Nations, **Global Dialogue on AI Governance and Independent International Scientific Panel on AI** — https://www.un.org/global-digital-compact/en/ai
13. Pew Research Center, **Americans and AI: 2026** — https://www.pewresearch.org/internet/2026/06/17/americans-and-ai-2026-chatbots-smart-devices-and-views-on-impact/
14. Stanford Institute for Human-Centered AI, **2026 AI Index Report — Public Opinion** — https://hai.stanford.edu/ai-index/2026-ai-index-report/public-opinion
15. C2PA, **Content Credentials technical specification 2.4** — https://spec.c2pa.org/specifications/specifications/2.4/specs/C2PA_Specification.html
16. Colorado Attorney General, **Artificial Intelligence policy and rulemaking** — https://coag.gov/ai/
17. White House, **National AI Legislative Framework**, March 20, 2026 — https://www.whitehouse.gov/releases/2026/03/president-donald-j-trump-unveils-national-ai-legislative-framework/
18. OpenAI, **Frontier Governance Framework** — https://openai.com/index/openai-frontier-governance-framework/
19. Anthropic, **Responsible Scaling Policy** — https://www.anthropic.com/responsible-scaling-policy
20. Google DeepMind, **Frontier Safety Framework** — https://deepmind.google/frontier-safety/

---

### Suggested citation

Schunk, David. "Checks and Balances for Artificial Intelligence: A Risk-Tiered Framework for Safety, Accountability, Public Trust, and Innovation." Version 1.0, September 18, 2026. DavidSchunk.com.

This paper represents the author's independent analysis. It is not legal advice and does not represent the position of any employer, government, standards body, or AI developer.
