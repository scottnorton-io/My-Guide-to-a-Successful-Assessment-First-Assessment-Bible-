# My Guide to a Successful Assessment (First Assessment Bible)

<aside>
🎯

This guide is designed to make a PCI assessment feel like *showing your work*, not *scrambling to survive an audit*.

</aside>

## The core idea: “Assessment-ready” is a system, not a season

A successful assessment is the byproduct of three things running continuously:

- **Truth**: the environment works the way you think it works.
- **Governance**: ownership, decision records, and policies match reality.
- **Evidence**: proof is produced as a routine exhaust of operations.

When those three are in place, an assessment becomes a controlled verification exercise.

---

## Part 0 — Vocabulary you must get right (or everything else collapses)

### 0.1 Define what you’re protecting

- **Account data**: include CHD and SAD (and related account data as applicable).
- **CDE/ADE**: where account data is stored, processed, transmitted.
- **Connected-to**: anything with a network path into the CDE that could affect security.
- **Impacting**: anything that can change security of CDE systems (identity, logging, DNS, CI/CD, hypervisor, etc.).
- **TPSP**: any third party with *access to* or *impact on* your CDE scope.

### 0.2 Your two outputs that drive everything

- **Scope package**: the definitive statement of scope (with proof).
- **Evidence map**: the “Requirement → control → proof → system of record” map.

If you don’t have these, every meeting becomes “what counts” debates.

---

## Part 1 — The First Assessment Reality (and how to win anyway)

First-year assessments are harder because you often lack historical evidence. Your objective is to be **honest, bounded, and defensible**:

- Where you have operational proof: show it.
- Where you do not yet have history: show **implementation**, **ownership**, **procedure**, and **forward-looking cadence** (and then start producing evidence immediately).

**Never bluff “operating effectiveness”** when you only have policy text. Instead, document:

- what exists today,
- what was tested,
- what is scheduled,
- what will be produced going forward.

---

## Part 2 — The Assessment Lifecycle (what happens in the real world)

A PCI assessment reliably follows this arc (even when people pretend it doesn’t):

1. **Scope discovery** (and late surprises)
2. **Evidence negotiation** (what counts, time windows, sampling)
3. **Validation** (inquiry/observation/inspection/testing)
4. **Exception handling** (gaps, partials, compensating controls)
5. **Report defensibility** (bounded language, traceable claims)

Your job is to pre-control each stage with artifacts and routines.

---

## Non-negotiable operating rule: “Assessment-ready” means ready *before kickoff*

- At kickoff, the assessed entity should expect to provide **complete, organized evidence immediately**.
- There is **zero acceptable delay** for missing evidence. The only legitimate “later” evidence is **remediation evidence** produced after a gap is identified and fixed.
- If key artifacts are missing, a good assessor will **stop and wait** rather than proceed on assumptions.
- The assessed entity is expected to have performed an **internal gap assessment (mock / pre-assessment)** prior to the formal engagement so the assessment is validation, not discovery.

---

## Part 3 — The “Scope Bible” (your #1 success factor)

Scope is not a statement. It’s an evidence chain.

### 3.1 The minimum scope-confirmation checklist (non-negotiable)

At a minimum, the assessed entity must be able to demonstrate:

- Identifying **all data flows** for payment stages (authorization, capture, settlement, chargebacks, refunds) and acceptance channels (card-present, card-not-present, e-commerce).
- Updating **data-flow diagrams** per Requirement 1.2.4.
- Identifying **all locations where account data is stored, processed, transmitted**, including: (1) outside the currently defined CDE, (2) apps that process CHD, (3) transmissions between systems/networks, and (4) backups.
- Identifying **all system components** in the CDE, connected to the CDE, or that could impact CDE security.
- Identifying **all segmentation controls** in use and the environment(s) from which the CDE is segmented, including justification for environments being out of scope.
- Identifying **all connections from third parties** with access to the CDE.
- Confirming that all identified data flows, account data, system components, segmentation controls, and third-party connections are included in scope.[[1]](https://grid-johansongroupllp.enterprise.slack.com/archives/C09MJSBRPME/p1769119016585839)

### 3.2 How scope breaks (three predictable failure modes)

1. **Diagram-based segmentation**
    - “Segmentation is a diagram,” not a tested control set.
2. **Milestone theater**
    - “We don’t store CHD,” but PAN exists in logs, backups, queues, exports.
3. **Governance fiction**
    - Policies describe a world that isn’t real; evidence reveals the truth.

### 3.3 Scope cadence: the thing people miss (Req 12.5.2 / 12.5.2.1)

Important nuance: the assessor’s role is to validate that the assessed entity **reviews their scope** on the required cadence; the assessor is not “doing scope” for the entity.[[1]](https://grid-johansongroupllp.enterprise.slack.com/archives/C09MJSBRPME/p1769119016585839)

For a first assessment, these sub-requirements may be **Not Applicable** with justification (first-year), but the *scope discipline* is still required to avoid late surprises.[[1]](https://grid-johansongroupllp.enterprise.slack.com/archives/C09MJSBRPME/p1769119016585839)

---

## Part 4 — Evidence that doesn’t collapse

### 4.1 Make an Evidence Map (Requirement → Proof)

For each requirement (and each control objective), define:

- **Control statement** (what is true)
- **Control owner** (human accountable)
- **System(s) of record** (where the proof lives)
- **Evidence type** (inquiry / observation / inspection / testing)
- **Time window** (what “covers the period”)
- **Sampling approach** (population, sample size, stratification)
- **Collection method** (manual vs automated)
- **Quality checks** (what makes it unacceptable)

This is what converts “audit” into “retrieval.”

### 4.2 Evidence rules (the ones that keep you defensible)

- Evidence must be **sufficient, relevant, and traceable** to the control claim.
- Every screenshot needs: **what**, **where**, **when**, **who**, and **how you know it’s production**.
- Prefer exports/logs/config dumps over screenshots when possible (less disputable).
- Treat each item as a courtroom exhibit:
    - provenance,
    - integrity,
    - time-bounded.

### 4.3 Naming conventions and structure (stop losing time)

Use a simple convention that supports sorting and review:

- `REQ-<n>.<sub>__<control>__<system>__<YYYY-MM>__<evidence-type>`

Example:

- `REQ-10.2__log-review__SIEM__2026-03__inspection.pdf`

---

## Part 5 — People: interviews, ownership, and “don’t guess”

### 5.1 Train your team on assessor mechanics

Before assessment, run a 45–60 minute session:

- What “inquiry vs observation vs inspection” means
- How to answer:
    - speak to what you do,
    - point to where evidence lives,
    - avoid speculation

### 5.2 Ownership is a control

If the requirement has no owner, the control doesn’t exist operationally.

- Assign owners early.
- Give owners evidence responsibilities (not just task responsibilities).

---

## Part 6 — Controls must work, not just exist

A written policy is not a control. A control is:

- implemented,
- operating,
- monitored,
- and produces proof.

Build a routine of:

- configuration checks,
- drift detection,
- access reviews,
- logging validation,
- vulnerability SLAs,
- change approvals.

---

## Part 7 — Pre-assessment “dress rehearsal” (the fastest way to reduce pain)

Run a pre-assessment that looks like the real one:

1. Freeze your current scope package version.
2. Execute the evidence map for a small, representative slice.
3. Identify where evidence is weak:
    - missing,
    - unclear,
    - not time-bounded,
    - not production,
    - not attributable.
4. Fix the evidence system, not just the artifacts.

---

## Part 8 — How to work with your assessor (and keep it smooth)

### 8.1 Establish rules of engagement early

- Single intake channel for evidence requests
- Single source of truth for scope artifacts
- Agreed time windows and sampling
- Agreed change-control boundaries during assessment

### 8.2 Use “bounded claims” language

Avoid absolutes. Prefer:

- “Based on inspection of X covering period Y…”
- “The control is implemented for systems A/B; systems C are out of scope because…”
- “Exceptions are documented in … with remediation plan …”

---

## Part 9 — Your 30/60/90-day First Assessment Plan

### First 30 days: stabilize scope + evidence system

- Build scope package v1 (data flows, diagrams, inventories, TPSPs)
- Build evidence map v1
- Establish evidence repository + naming conventions

### Next 30 days: prove operation

- Start producing recurring evidence (logs, scans, reviews)
- Run mock interviews + spot-check controls
- Close top risk gaps that will block report defensibility

### Final 30 days: compress execution risk

- Pre-assessment dry run on the hardest requirements
- Lock scope package version for assessment start
- Ensure every “must show” item has a retrieval path and owner

---

## Appendix A — What “good” looks like (quick diagnostics)

You are assessment-ready when:

- scope is explainable in 10 minutes with diagrams and inventories,
- every requirement has an owner and a proof path,
- evidence is produced monthly/quarterly by default,
- exceptions are documented and bounded,
- the assessment feels like retrieval, not invention.

---

## Appendix B — Minimal artifact set (starter list)

**Scope artifacts**

- Data flow diagrams (per acceptance channel + payment stages)
- Network diagrams + segmentation boundaries
- Inventory: in-scope system components and “impacting” systems
- Inventory: account data locations (including logs/backups/queues)
- TPSP list + access paths + responsibilities

**Evidence system artifacts**

- Evidence map (Requirement → Proof)
- Evidence repository structure + naming standards
- Cadence calendar (what evidence is produced when)
- Exception register (with dates, scope, and remediation)

**Governance artifacts**

- Program charter / governance
- Policies + procedures (aligned to reality)
- Risk decisions (TRAs where applicable)
- Change control + approvals + review records

<aside>
🧱

If you do only one thing: build the scope package and evidence map. Everything else becomes easier once those exist.

</aside>
