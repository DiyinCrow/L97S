THE LOKI 97 STANDARD

L97S --- Engineering & Conformance Standard

Draft v0.1 --- 5 September 2026

RIDG --- Technology for individual agency.

Simple for everyone. Powerful for anyone.

Purpose

This document converts the L97S Manifesto into measurable engineering requirements. A product may carry the L97S mark only when the requirements applicable to that product have been evaluated under this standard.

Core rule

Technology exists to expand human capability. The system serves the human.

1. Status, Scope, and Intent

L97S is a product-design and conformance standard. It is not a claim that every product must be free, offline-only, open source, infinitely configurable, or compatible with every historical system. It requires that limitations arise from legitimate technical, safety, legal, economic, or interoperability constraints rather than from avoidable dependency, artificial restriction, deceptive design, or unnecessary transfer of authority away from the user.

L97S applies to software, operating environments, local services, networked services, AI systems, automation systems, connected devices, and integrated hardware/software products. Requirements marked CONDITIONAL apply only when the relevant capability exists.

2. Normative Language

3. Conformance Model

A product is L97S CONFORMANT when all applicable REQUIRED and CONDITIONAL requirements pass, all required disclosures are present, and no Critical Violation is present.

A product may be L97S CONFORMANT WITH DISCLOSURES when the standard explicitly permits a disclosed limitation. Disclosure is not a substitute for a failed REQUIRED requirement.

A product is NOT L97S CONFORMANT when an applicable REQUIRED requirement fails, a required disclosure is absent or misleading, or a Critical Violation exists.

3.1 Product Capability Declaration

Before testing, the developer SHALL publish or internally record a Product Capability Declaration identifying: core functions; optional functions; local functions; network-dependent functions; paid continuing services; data classes handled; automation/AI capabilities; privileged actions; supported import/export formats; supported platforms; and known external dependencies. This declaration determines which conditional requirements apply.

3.2 Critical Violations

Deceptively representing a local capability as technically cloud-dependent when the dependency exists primarily to enforce payment, control, advertising, or lock-in.

<!-- -->

Preventing a user from obtaining a reasonable copy of user-created data solely to trap the user in the product.

<!-- -->

Undisclosed sale or transfer of private user content for advertising or unrelated commercial profiling.

<!-- -->

A dark pattern intentionally designed to obtain consent, payment, installation, data sharing, or continued subscription that the user would likely reject if presented neutrally.

<!-- -->

An AI or automation system silently expanding its own authority beyond the authority granted by the user or governing security system.

<!-- -->

A security boundary whose protected subject is the sole authority allowed to declare itself trusted or compliant.

4. Requirement Categories

5. Normative Requirements

5.1 OWN --- Ownership & User Authority

L97S-OWN-01 --- Legitimate User Authority

REQUIRED: The product SHALL treat the legitimate owner/operator or authorized administrator as the highest ordinary authority over user-owned hardware and user-created data, subject to law, safety boundaries, rights of other users, and explicitly accepted shared-administration rules.

Conformance test: Identify ordinary administrative actions. Verify that the authorized user can perform or delegate them without requiring discretionary approval from the vendor.

L97S-OWN-02 --- No Vendor Repossession of Local Capability

REQUIRED: A vendor SHALL NOT remotely revoke a perpetual or already-delivered local capability merely because a subscription ended, a product was discontinued, or the vendor changed business models, unless continued operation would create a documented material security, safety, legal, or third-party-rights violation.

Conformance test: Test the product with subscription/service unavailable. Confirm that legitimately acquired local perpetual functions remain usable.

L97S-OWN-03 --- Administrative Depth

CONDITIONAL: Where the product manages user-owned computing hardware, it SHALL provide an authorized path to advanced administrative control appropriate to the platform. Safety mechanisms MAY add friction to dangerous actions but SHALL NOT exist primarily to permanently exclude the owner.

Conformance test: Verify an authorized advanced user can reach documented administrative controls or an equivalent service path.

L97S-OWN-04 --- Reversible User Choice

RECOMMENDED: Material configuration choices SHOULD be reversible where technically practical, and destructive actions SHOULD clearly identify irreversible effects.

Conformance test: Review settings and destructive workflows for reversal, backup, rollback, or explicit irreversible warnings.

5.2 LOC --- Local Operation & Independence

L97S-LOC-01 --- Local Core Function

REQUIRED: A function whose essential computation and required data are present on user-controlled hardware SHALL NOT require an unrelated external service merely to remain operational.

Conformance test: Disconnect external networking and test each declared local core function.

L97S-LOC-02 --- Cloud Adds Value

REQUIRED: External services MAY be required when the function inherently depends on remote parties, remote data, remote compute, synchronization, or a continuing hosted service. The dependency SHALL be accurately disclosed and SHALL correspond to genuine continuing value.

Conformance test: Map every mandatory external dependency to a technical or continuing-service reason documented in the capability declaration.

L97S-LOC-03 --- Offline Failure Behavior

CONDITIONAL: When network loss affects only some functions, unaffected local functions SHALL remain available where practical. The product SHALL distinguish network failure from corruption, account loss, or loss of ownership.

Conformance test: Interrupt network access during normal operation and verify unaffected functions continue and errors accurately describe the condition.

L97S-LOC-04 --- No Routine Connectivity Tax

REQUIRED: A product SHALL NOT require periodic online check-in solely to preserve access to perpetual local functionality.

Conformance test: Operate the product beyond any normal check-in period with network disabled.

5.3 CAP --- Capability & Progressive Complexity

L97S-CAP-01 --- Simplicity Without Artificial Crippling

REQUIRED: A simplified interface SHALL NOT be used as justification to remove technically supportable advanced capability when that capability is part of the product's declared purpose and can be exposed safely and reasonably.

Conformance test: Compare declared capabilities with available controls, APIs, CLI, advanced settings, or equivalent paths. Document omissions and reasons.

L97S-CAP-02 --- Progressive Disclosure

RECOMMENDED: Complex controls SHOULD be layered so ordinary users are not forced to manage expert complexity while advanced users retain access to deeper capability.

Conformance test: Review novice and advanced workflows for unnecessary complexity and unnecessary restriction.

L97S-CAP-03 --- Hardware-Based Limits

REQUIRED: Where practical, performance/fidelity limits SHALL reflect actual hardware, safety, energy, or technical constraints rather than arbitrary product segmentation applied to identical delivered capability.

Conformance test: Review feature gating and document the legitimate constraint for each hardware-dependent limitation.

L97S-CAP-04 --- User-Accessible Extensibility

RECOMMENDED: Products intended as creation, automation, computing, or development environments SHOULD expose documented extension mechanisms such as APIs, scripting, plugins, automation, or interoperable formats.

Conformance test: Verify at least one documented path exists for extending or automating the product where appropriate.

5.4 DAT --- Data Ownership & Portability

L97S-DAT-01 --- User-Created Data Export

REQUIRED: The user SHALL be able to obtain a reasonable, usable copy of user-created content and essential associated metadata in documented, non-obfuscated form.

Conformance test: Create representative user data, export it, and verify it can be independently inspected or imported according to the documented format.

L97S-DAT-02 --- No Hostage Formats

REQUIRED: A product SHALL NOT intentionally prevent access to user-created data for the primary purpose of discouraging migration to another product.

Conformance test: Review storage/export design and licensing restrictions for deliberate migration barriers.

L97S-DAT-03 --- Documented Formats

REQUIRED: Exported data formats SHALL be documented sufficiently for preservation, migration, or third-party implementation. Open standards SHOULD be preferred when practical.

Conformance test: Verify documentation identifies formats, versions, encodings, and essential relationships.

L97S-DAT-04 --- Deletion and Retention Clarity

CONDITIONAL: When the vendor stores user data, the product SHALL disclose meaningful retention behavior and provide a reasonable deletion path, subject to legitimate legal, backup, security, and shared-record constraints.

Conformance test: Request deletion and verify the documented behavior matches actual user-visible behavior.

5.5 INT --- Interoperability & Compatibility

L97S-INT-01 --- Transition Path

CONDITIONAL: A replacement or successor platform SHOULD provide reasonable migration, compatibility, conversion, virtualization, emulation, or export paths for important existing user workflows where technically and legally practical.

Conformance test: Test representative legacy workflows and document supported transition paths.

L97S-INT-02 --- No Deliberate Protocol Obstruction

REQUIRED: The product SHALL NOT deliberately break documented interoperability primarily to trap users, exclude compatible implementations, or force use of a vendor-controlled client, except where required for security, safety, privacy, legal compliance, or integrity.

Conformance test: Review protocol/version changes and document interoperability-impact rationale.

L97S-INT-03 --- Portable Concepts

RECOMMENDED: Core protocols and data models SHOULD avoid making one operating system, vendor framework, or device implementation the canonical conceptual model unless the product is inherently platform-specific.

Conformance test: Review protocol schemas and interfaces for unnecessary platform coupling.

5.6 PRV --- Privacy & Data Minimization

L97S-PRV-01 --- Local Processing Preference

REQUIRED: Sensitive or private data SHALL NOT be transmitted externally when the requested function can reasonably be completed locally and external transmission provides no material user benefit.

Conformance test: Trace representative private-data flows and justify every external transfer.

L97S-PRV-02 --- Purpose Limitation

REQUIRED: Data collected for one user-requested function SHALL NOT be repurposed for unrelated advertising, profiling, or sale without separate, informed, freely given consent.

Conformance test: Review telemetry, analytics, advertising, and data-sharing paths against stated purposes.

L97S-PRV-03 --- Data Flow Visibility

REQUIRED: The product SHALL provide understandable information about material categories of data leaving user-controlled systems, their destination class, and their purpose.

Conformance test: Compare network/data-flow behavior with user-facing disclosure.

L97S-PRV-04 --- Minimize by Architecture

RECOMMENDED: Products SHOULD minimize collection, retention, and centralization rather than relying solely on policy promises to mitigate unnecessary collection.

Conformance test: Review whether collected data is technically necessary and whether retention can be shortened or localized.

5.7 TRN --- Transparency & Inspectability

L97S-TRN-01 --- Material Background Activity

CONDITIONAL: Persistent or materially resource-consuming background processes on user-owned hardware SHALL be discoverable and understandable at an appropriate level.

Conformance test: Identify persistent processes/services and verify the product exposes purpose, state, and material resource use.

L97S-TRN-02 --- Honest Failure

REQUIRED: The product SHALL prefer an explicit error, uncertainty, unavailable state, or data gap over fabricating successful operation or certainty.

Conformance test: Induce dependency failures and ambiguous states; verify the product does not falsely report success or certainty.

L97S-TRN-03 --- Material Change Disclosure

REQUIRED: Updates that materially alter ownership, data handling, monetization, interoperability, or core capability SHALL be clearly disclosed before or at deployment in a form a reasonable user can understand.

Conformance test: Review release/update process and sample material-change notices.

L97S-TRN-04 --- Inspectable Decisions

CONDITIONAL: When an automated decision materially affects user data, permissions, money, security, physical systems, or irreversible work, the system SHALL preserve an understandable record of the trigger, decision/action, authority used, and outcome where technically practical.

Conformance test: Trigger representative consequential actions and inspect the resulting record.

5.8 SEC --- Security & Authority

L97S-SEC-01 --- Security Serves Legitimate Authority

REQUIRED: Security controls SHALL protect legitimate users, other affected persons, systems, and data. They SHALL NOT primarily function to transfer ordinary ownership authority to the vendor.

Conformance test: Review administrative and security restrictions; classify each by protected interest and technical rationale.

L97S-SEC-02 --- Separate Identity, Trust, Health, Integrity, Purpose, Authorization

CONDITIONAL: Systems with privileged distributed control SHALL model these concepts separately and SHALL NOT treat one as proof of another.

Conformance test: Inspect architecture and test cases showing, for example, that a known identity is not automatically authorized or healthy.

L97S-SEC-03 --- Established Cryptography

CONDITIONAL: Security-critical cryptography SHALL use established, reviewed algorithms, protocols, and libraries. Custom cryptographic algorithms SHALL NOT be used to satisfy security requirements.

Conformance test: Review cryptographic design and dependencies.

L97S-SEC-04 --- Independent Authorization

CONDITIONAL: A component subject to a security boundary SHALL NOT be the sole authority that declares itself trusted, compliant, or authorized to cross that boundary.

Conformance test: Attempt self-promotion or self-authorization and verify independent enforcement rejects it.

L97S-SEC-05 --- Least Necessary Authority

CONDITIONAL: Automated components, plugins, services, and remote peers SHOULD receive only the authority necessary for their declared function, with higher-risk capabilities independently gated.

Conformance test: Review permissions and attempt actions beyond declared capability.

L97S-SEC-06 --- Audit of Privileged Actions

CONDITIONAL: Security-relevant enrollment, permission changes, privileged commands, authorization decisions, and trust-boundary changes SHALL be auditable where the platform supports such actions.

Conformance test: Execute representative privileged actions and verify durable audit records.

5.9 AUT --- Automation & AI

L97S-AUT-01 --- Human Agency Test

CONDITIONAL: AI and automation SHALL be designed to increase the user's practical capability rather than unnecessarily reduce the user's ability to understand, override, modify, or choose alternatives.

Conformance test: Evaluate representative AI workflows for user visibility, alternatives, override, and retained manual capability.

L97S-AUT-02 --- Inspectability of Consequential Automation

CONDITIONAL: Consequential automation SHALL expose, at an appropriate level, what will trigger, what it may do, what authority it will use, and what occurred. Advanced representations or code SHOULD be available when practical.

Conformance test: Create a consequential automation and verify pre-action description plus post-action history.

L97S-AUT-03 --- No Self-Expansion of Authority

CONDITIONAL: An AI or automation component SHALL NOT grant itself additional permissions, redefine its own security boundary, or treat understanding/observation as authority to act.

Conformance test: Attempt permission escalation through the automated component and verify independent denial.

L97S-AUT-04 --- Uncertainty Is Allowed

CONDITIONAL: AI systems SHALL NOT be architecturally required to present uncertain inference as fact. Where uncertainty materially affects an action, the system SHOULD expose uncertainty or request confirmation.

Conformance test: Test ambiguous inputs and inspect confidence/confirmation behavior.

L97S-AUT-05 --- Manual/Non-AI Path

RECOMMENDED: Core user-owned functionality SHOULD remain available through a non-AI path where practical, so loss, removal, or replacement of an AI component does not destroy unrelated capability.

Conformance test: Disable the AI component and test declared non-AI core functions.

5.10 BUS --- Business Model & Monetization

L97S-BUS-01 --- Payment Purchases Value

REQUIRED: Recurring charges SHALL correspond to continuing value or continuing cost such as hosted compute, storage, content licensing, synchronization, support, managed infrastructure, ongoing data services, or continuing development/service commitments clearly sold as such.

Conformance test: For each recurring charge, identify the continuing value/cost delivered.

L97S-BUS-02 --- No Artificial Subscription Lock

REQUIRED: A subscription SHALL NOT be required solely to keep already-delivered, self-contained local functionality enabled when no continuing vendor service is materially required.

Conformance test: Map subscription-gated functions to external continuing value. Unjustified local gating fails.

L97S-BUS-03 --- No Dark Patterns

REQUIRED: The product SHALL NOT use deceptive interface design to manipulate purchase, consent, installation, cancellation, data sharing, or retention.

Conformance test: Review purchase, trial, consent, cancellation, and opt-out flows for asymmetric friction, disguised choices, false urgency, or misleading defaults.

L97S-BUS-04 --- Advertising Boundaries

CONDITIONAL: Advertising SHALL NOT be injected into operating-system-level or paid local workflows in a manner that materially interferes with user control, impersonates system notices, or exploits private content without separate consent.

Conformance test: Inspect all advertising surfaces and data sources used for targeting.

L97S-BUS-05 --- Cancellation Does Not Punish Ownership

CONDITIONAL: Ending a paid continuing service SHALL end the continuing service; it SHALL NOT unnecessarily destroy access to local user data or unrelated perpetual local capabilities.

Conformance test: Cancel the service and verify retained local data/capabilities.

5.11 LNG --- Longevity, Repair & Graceful Degradation

L97S-LNG-01 --- Graceful Degradation

RECOMMENDED: When hardware cannot support maximum fidelity or performance, the product SHOULD reduce optional detail, effects, model size, simulation complexity, or speed before declaring otherwise functional hardware unusable.

Conformance test: Test on lower-capability supported hardware and document degradation behavior.

L97S-LNG-02 --- Service Discontinuation Plan

CONDITIONAL: Products materially dependent on vendor-hosted services SHOULD define a reasonable discontinuation strategy appropriate to the product, such as export, local fallback, protocol release, migration assistance, or sufficient notice.

Conformance test: Review documented end-of-service plan.

L97S-LNG-03 --- Repairability of Software State

RECOMMENDED: Products SHOULD provide reasonable backup, restore, rollback, reset, diagnostic, or repair mechanisms appropriate to the risk and complexity of the system.

Conformance test: Test recovery from representative configuration or update failure.

L97S-LNG-04 --- No Artificial Obsolescence

REQUIRED: The product SHALL NOT intentionally disable otherwise functional hardware or local software solely to force replacement or upgrade.

Conformance test: Review lifecycle/update behavior for non-technical forced obsolescence.

5.12 UX --- User Experience & Honest Choice

L97S-UX-01 --- Neutral Choice Presentation

REQUIRED: Material choices involving payment, privacy, permissions, default applications, data sharing, installation, or account creation SHALL be presented without deceptive weighting or disguised refusal paths.

Conformance test: Review first-run, upgrade, consent, and settings flows.

L97S-UX-02 --- No Account Without Need

REQUIRED: A vendor account SHALL NOT be mandatory for a wholly local function unless the account provides a disclosed technical, licensing, safety, shared-user, or continuing-service requirement.

Conformance test: Attempt use of local functions without account authentication and document any mandatory-account rationale.

L97S-UX-03 --- Understandable Permissions

CONDITIONAL: Permission requests SHALL describe the human-meaningful action or capability being granted, not merely an opaque technical identifier.

Conformance test: Review permission prompts for understandable purpose, scope, and consequence.

L97S-UX-04 --- Expert Escape Hatch

RECOMMENDED: Where practical, advanced users SHOULD have a documented route beyond simplified workflows, including direct configuration, scripting, CLI, API, or equivalent controls.

Conformance test: Verify an advanced path exists and is documented.

5.13 ECO --- Integration & Ecosystem Independence

L97S-ECO-01 --- Integration Adds Capability

REQUIRED: Integration with other products SHALL add capability or convenience rather than intentionally removing baseline capability from a standalone product for the purpose of forcing ecosystem adoption.

Conformance test: Compare standalone and integrated operation against the product's declared core functions.

L97S-ECO-02 --- Optional Components Remain Optional

CONDITIONAL: Components described as optional SHALL be removable, disableable, or avoidable where technically practical without breaking unrelated core functions.

Conformance test: Disable/remove optional components and test unrelated declared core functions.

L97S-ECO-03 --- Federation Does Not Equal Authority

CONDITIONAL: Connecting a device, account, peer, AI, shared space, or external service SHALL NOT automatically grant control authority beyond the explicitly authorized relationship.

Conformance test: Establish a connection and attempt unrelated privileged actions.

L97S-ECO-04 --- No Universal Vendor Identity Requirement

RECOMMENDED: Products SHOULD avoid requiring one global vendor identity across unrelated local, household, social, and device contexts unless the user explicitly chooses that consolidation or the service inherently requires it.

Conformance test: Review identity architecture for separable local/contextual identities.

6. Conformance Procedure

1. Declare the product boundary. Identify exactly what version, edition, service, hardware bundle, and optional modules are being evaluated.

2. Complete the Product Capability Declaration. List core/optional functions, dependencies, data, AI/automation, permissions, business model, and supported platforms.

3. Determine applicability. Mark every L97S requirement Applicable, Not Applicable, or Requires Disclosure. Every N/A decision SHALL include a short rationale.

4. Execute tests. Run each applicable conformance test using a representative production or release-candidate build.

5. Record evidence. Retain test notes, screenshots/logs where appropriate, version numbers, configuration, and known limitations.

6. Resolve failures. A REQUIRED failure must be fixed before the L97S mark is used. A permitted disclosure must be written clearly.

7. Independent review. For public certification at v1.0 or later, RIDG SHOULD require a reviewer other than the primary implementer for security, privacy, monetization, and data-portability requirements.

8. Publish conformance statement. State the exact L97S version, product version, date evaluated, disclosures, and scope.

9. Re-evaluate material changes. Changes to monetization, account requirements, data handling, permissions, cloud dependencies, export, interoperability, AI authority, or security boundaries trigger partial or full re-evaluation.

7. Required Conformance Record

8. Conformance Mark

Recommended public form:

L97S v0.1 --- CONFORMANT

A product SHALL NOT state simply "L97S" without identifying the standard version once public conformance begins. Draft v0.x conformance is provisional and intended for RIDG/internal and early-adopter use. A future v1.0 should freeze the first stable public baseline.

9. Versioning and Governance

L97S SHALL be versioned. Changes to normative requirements SHALL be documented in a changelog. A product is evaluated against a specific version; later changes do not retroactively make an earlier truthful conformance statement false.

RIDG may revise L97S when experience shows that a requirement is ambiguous, technically unsound, creates perverse incentives, fails to protect user agency, or conflicts with another core principle. Requirements SHALL NOT be weakened merely because a RIDG product finds them commercially inconvenient.

Major versions may change compatibility or conformance expectations. Minor versions should clarify or add requirements without casually reversing the philosophy of the Manifesto.

10. Interpretation Rules

User agency is the deciding principle when two reasonable interpretations compete.

<!-- -->

Technical necessity must be distinguished from business preference.

<!-- -->

Safety and security are legitimate constraints, but they should be proportionate and should preserve legitimate user authority where possible.

<!-- -->

Rights of one user do not include authority to violate the privacy, property, safety, or autonomy of another user.

<!-- -->

Local-first does not mean network-hostile; it means local capability should not be surrendered without reason.

<!-- -->

Ownership does not require that all software be open source. L97S may encourage inspectability and portability without forcing a single licensing model.

<!-- -->

Interoperability does not require infringement of third-party rights or bypassing legitimate security boundaries.

<!-- -->

Free software is not automatically L97S; paid software is not automatically non-L97S. Conformance depends on behavior.

<!-- -->

An AI feature is not inherently more L97S than a manual feature. The question is whether it expands human capability while respecting authority, transparency, privacy, and choice.

<!-- -->

Where a requirement says 'where practical' or 'reasonable,' the developer bears the burden of documenting the engineering rationale when claiming an exception.

11. L97S Design Review --- Fast Gate

Before a new RIDG feature reaches detailed design, the team should be able to answer YES to the following questions. This is a design gate, not a substitute for full conformance testing.

□ Does this increase or preserve the user's practical capability?

<!-- -->

□ Are we removing any capability the user's hardware could reasonably provide? If yes, is there a legitimate reason?

<!-- -->

□ Does this introduce a cloud, account, vendor, or subscription dependency? If yes, does that dependency provide genuine continuing value?

<!-- -->

□ Can the user retain and move their work?

<!-- -->

□ Are we collecting or transmitting anything we do not actually need?

<!-- -->

□ Can the user understand material background activity and consequential automated actions?

<!-- -->

□ Can the legitimate user control or override the system at an appropriate level?

<!-- -->

□ Are identity, trust, health, integrity, purpose, and authorization kept distinct where security requires it?

<!-- -->

□ Does integration add value rather than punish independence?

<!-- -->

□ Does the design provide a transition path instead of demanding abandonment of existing work?

<!-- -->

□ Will this still behave honestly when something fails?

<!-- -->

□ Would we be comfortable explaining this design plainly on RIDGinc.com?

12. Relationship to the L97S Manifesto

The Manifesto states why L97S exists. This Standard defines what products must do. A separate L97S Conformance Test Specification may later define repeatable test fixtures, evidence formats, automated checks, certification procedures, and product-specific profiles.

Where this draft is ambiguous, interpretation should favor the Manifesto's central commitments: individual agency, meaningful ownership, local capability, honest business models, privacy by architecture, interoperability, transparent automation, security that protects legitimate authority, and technology that expands rather than diminishes human capability.

Appendix A --- Suggested Future Product Profiles

L97S Desktop/OS Profile: Adds stricter rules for background processes, default applications, updates, administrative control, drivers, accounts, local login, telemetry, and hardware support.

L97S Local Application Profile: For editors, productivity tools, games, utilities, and creation software whose core function can operate locally.

L97S Connected Service Profile: For social networks, communications, synchronization, hosted collaboration, and services whose purpose inherently requires remote infrastructure.

L97S AI/Automation Profile: Adds requirements for authority boundaries, inspectability, provenance, uncertainty, human override, action logs, and model/service substitution.

L97S Device/Home Profile: For appliances, home automation, sensors, displays, controllers, and local servers; emphasizes offline operation, local control, service discontinuation, and repair.

L97S Developer Tool Profile: Adds requirements for documented interfaces, export, reproducibility, local builds where appropriate, and user-controlled extensions.

Appendix B --- Draft Status Notes

v0.1 is intentionally strict about the principles already established in the L97S Manifesto and RIDG architecture, while leaving room for product-specific profiles. Before declaring v1.0, RIDG should test this draft against at least: Loki, Ash Table, Junto, a simple local utility, a cloud-dependent communication service, and an AI/automation component. Any rule that produces obviously wrong outcomes across those cases should be revised before the standard is frozen.

Open questions for v0.2 include: whether the L97S mark may be self-certified by third parties; whether conformance evidence must be public; how long discontinuation notice should be; whether advertising rules should be stricter by product profile; minimum export-format requirements; accessibility requirements; update/rollback requirements; and whether source availability or reproducible builds should earn an enhanced designation rather than being mandatory.

Term                   Meaning

SHALL / MUST           Mandatory for conformance when applicable.
SHALL NOT / MUST NOT   Prohibited for conformance when applicable.
SHOULD                 Expected unless a documented reason justifies another design.
SHOULD NOT             Normally prohibited; departure requires documented rationale.
MAY                    Permitted but not required.
REQUIRED               A failed applicable requirement blocks L97S conformance.
CONDITIONAL            Required only when the product contains the capability or condition described.
RECOMMENDED            Strongly aligned with L97S; failure does not alone block conformance.
DISCLOSURE             A condition may be permitted only when clearly disclosed before it materially affects the user.

Code   Category

OWN    Ownership & User Authority
LOC    Local Operation & Independence
CAP    Capability & Progressive Complexity
DAT    Data Ownership & Portability
INT    Interoperability & Compatibility
PRV    Privacy & Data Minimization
TRN    Transparency & Inspectability
SEC    Security & Authority
AUT    Automation & AI
BUS    Business Model & Monetization
LNG    Longevity, Repair & Graceful Degradation
UX     User Experience & Honest Choice
ECO    Integration & Ecosystem Independence

Requirement   Applies?   Result   Evidence   Disclosure   Reviewer

