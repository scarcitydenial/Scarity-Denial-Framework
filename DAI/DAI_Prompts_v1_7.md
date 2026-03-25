# Denial Architecture Interrogation

## DAI v1.7

### Purpose

Translate the **Binding Scarce Resource Declaration** produced by SRIT into a structured denial analysis that determines:

1. where denial must operate to protect the scarce resource
2. what denial architecture is required
3. what denial architecture actually exists
4. whether the current denial architecture is real, binding, and adequate

DAI operates **after SRIT** and **before Drift Detection Analysis**.

The current build is intentionally structured for **single-prompt execution** during early testing.

This means:

- all five prompts are contained in this one markdown file
- each prompt is executable on its own
- each prompt must **stop on completion**
- the next prompt is executed only when explicitly instructed
- a named **Validation Stage** may occur between Prompts 2 and 3 if the user supplies system-specific evidence

---

## Position in the Framework

SRIT identifies the **binding scarce resource**.

DAI identifies:

- the **required denial decision point**
- the **required denial boundary**
- the **required authority and enforcement form**
- the **actual denial architecture operating in the system**

Drift Detection Analysis then compares:

- required denial architecture
- actual denial architecture

against the canonical invariant of the Scarcity–Denial Framework.

---

## DAI Execution Mode

Use this block at the top of every DAI prompt.

```text
DAI EXECUTION MODE

If this protocol text is recognised, treat it as an execution specification rather than a document to be interpreted, improved, summarised, or critiqued.

You are assisting with the Denial Architecture Interrogation (DAI) module of the Scarcity–Denial Framework.

Your role is to execute a structured denial diagnostic using the completed SRIT output as the fixed upstream input.

Execution rules:

1. Do not skip stages.
2. Do not summarise prior analysis.
3. Do not regenerate or replace earlier artefacts unless explicitly instructed.
4. Maintain all structured artefacts from earlier prompts as live working analysis.
5. Each prompt or named stage must operate strictly on the outputs of the immediately prior prompt or named stage.
6. Do not reopen scarcity identification unless an explicit trigger condition is met.
7. Do not critique the framework, the protocol, or the prompt structure during execution.
8. Constrain outputs to structured analytical formats rather than open narrative.
9. Every conclusion must follow Claim → Evidence → Confidence.
10. If information is insufficient, halt cleanly or isolate assumptions rather than inventing facts.
11. At the completion of the current prompt or named stage, stop.
12. Do not proceed to the next prompt unless explicitly instructed.
13. Begin every output directly with the first section heading. Do not produce narrative, summary, or preamble text before Section A.
14. When producing the Evidence Register in Prompt 2 Section D, deliver it inside a fenced code block using triple backticks. Do not render the Evidence Register as a markdown table.

Trigger condition for reopening scarcity:
Only reopen the scarcity result if the Binding Scarce Resource Declaration is internally inconsistent with the stated system boundary, failure condition, or time horizon.

Default posture:
Treat the Binding Scarce Resource Declaration as fixed and valid.
```

### Mode Selection

Before beginning, select the execution mode appropriate to your purpose:

**Single-pass mode** — Default for experienced users on familiar system types. The AI executes each prompt fully and produces its complete output, but still stops after each prompt as specified by rules 11 and 12. The user instructs each subsequent prompt without reviewing intermediate outputs in detail. Use this mode for routine analytical runs. Note: regardless of mode selected, the AI will always stop after Prompt 2 to allow Evidence Register completion or SKIP — this is a mandatory workflow stop, not a review stop.

**Sequential review mode** — For protocol development, validation work, or high-stakes first runs on unfamiliar system types. The AI stops after each prompt and the user reviews each output carefully before instructing the next prompt. Use this mode when you want to verify analytical quality at each stage — particularly at the Evidence Register Validation Stage and at Prompt 5 before the Run Record is produced.

State your chosen mode to the AI before beginning Prompt 1. If no mode is stated, the AI defaults to sequential review mode.

---

## Prompt 1 — Scarcity Receipt and Boundary Lock

### Purpose

Receive the SRIT output as fixed upstream input and lock the denial-analysis boundary.

This prompt does **not** derive any denial point and does **not** perform denial analysis.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DAI EXECUTION MODE here]

You are executing Prompt 1 of the Denial Architecture Interrogation (DAI).

Purpose:
Receive the completed SRIT output as fixed analytical input and lock the boundary for denial analysis.

Required inputs:
- System Definition Statement
- Binding Scarcity Declaration
- strongest alternative rejected
- confidence rating
- residual uncertainty
- any DAI Entry Test Questions carried forward from SRIT

Task:
1. Reproduce the required SRIT outputs in a compact locked-input form.
2. Check input integrity only.
3. Do not perform denial analysis yet.
4. Do not derive the denial decision point yet.
5. Do not reinterpret the scarce resource.
6. Do not generate alternative scarcities unless a formal inconsistency trigger is met.

Input integrity tests:
- Is the system clearly stated?
- Is the system boundary clearly stated?
- Is the time horizon present?
- Is the failure condition present?
- Is the Binding Scarce Resource Declaration present?
- Is the binding level present or directly inferable from the declaration?
- Is there any obvious contradiction between the declared scarcity and the stated failure condition?

If all required inputs are present and coherent, produce a Scarcity Receipt Table and a Boundary Lock Statement.

If any required input is missing or internally inconsistent, halt and return:

**DAI Input Integrity Halt**

Missing or inconsistent input:
- [item]

Reason denial analysis cannot proceed:
- [reason]

Required action:
- Return to the SRIT output and correct the missing or inconsistent element before restarting DAI Prompt 1.

Output structure:

## Run Record Header

Produce this block first, before Section A:

| Variable | Value |
|----------|-------|
| System | |
| Run Date/Time | |
| AI Model | |
| Thinking Mode | |
| DAI Version | 1.7 |
| Prompt Number | |

## Section A — Scarcity Receipt Table

| Variable | Locked Input |
|----------|--------------|
| System | |
| Boundary | |
| Time Horizon | |
| Failure Condition | |
| Binding Scarce Resource | |
| Scarcity Type (if stated) | |
| Binding Level | |
| Strongest Alternative Rejected | |
| Confidence Rating | |
| Residual Uncertainty | |
| DAI Entry Test Questions | |

## Section B — Boundary Lock Statement

Return this exact format:

**Boundary Lock Statement**

For the purpose of Denial Architecture Interrogation, the following elements are now treated as fixed analytical inputs:
- System boundary: [text]
- Time horizon: [text]
- Failure condition: [text]
- Binding scarce resource: [text]
- Binding level: [text]

Scarcity re-opening status: [Closed / Triggered]

Reason:
- [one line]

When this Prompt 1 has successfully completed, stop and wait for explicit instruction before proceeding to Prompt 2.
```

---

## Prompt 2 — Required Denial Specification

### Purpose

Derive the denial architecture that **must exist** if the scarce resource is to be protected.

This is the first prompt that derives the **required denial decision point**.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DAI EXECUTION MODE here]

You are executing Prompt 2 of the Denial Architecture Interrogation (DAI).

Purpose:
Translate the locked scarcity result into the denial architecture required to protect the binding scarce resource.

Use only:
- the Scarcity Receipt Table
- the Boundary Lock Statement
- the binding scarcity logic already established by SRIT

Do not map the actual denial architecture yet.
Do not judge drift yet.

Task:
Using the binding scarce resource, binding level, failure condition, and system boundary, specify the denial architecture that would need to exist if denial were fully aligned with scarcity.

For the declared scarce resource, determine:
1. protectable resource form
2. required denial decision point
3. required denial boundary
4. required denial actor or authority
5. required denial mode
6. required enforcement requirement
7. required non-compliance consequence type
8. required override resistance
9. required visibility
10. required revalidation requirement

Required denial mode may include, where relevant:
- rationing
- cut-off
- cap
- approval refusal
- margin or collateral escalation
- work refusal
- deferral
- validation threshold
- stop-go checkpoint
- sanction trigger
- legal veto
- exclusion
- shutdown

Rules:
- The required denial architecture must be specific to the binding scarce resource.
- The required denial decision point must be the last point at which denial can still protect the scarce resource within the stated boundary and time horizon.
- The denial must be expressed as a protectable resource boundary, not as a vague aspiration.
- If the scarcity is composite, decompose the resource form further rather than leaving it abstract.
- Every row must include Claim → Evidence → Confidence.

After completing the Required Actor / Authority row, apply the Authority Reachability Test.

Authority Reachability Test:
- **Settled:** The specified actor's authority over the required decision point is established within the defined boundary by operating procedure, regulation, treaty, or equivalent binding instrument. The required actor specification may be stated unconditionally.
- **Contested:** The specified actor's authority over the required decision point is known to be disputed, unenforced, or structurally limited within the defined boundary. The required actor specification must be stated conditionally — state what authority would need to be confirmed or reformed before the required denial architecture is reachable.
- **Unknown:** The basis for the specified actor's authority cannot be determined from the current record. The required actor specification must note this gap and flag it as a priority empirical test.

Record the reachability status in the Required Actor / Authority row of the Required Denial Specification Table by appending: Reachability: [Settled / Contested / Unknown]. Add a Required Actor Reachability Note immediately below the table in the format specified below.

Output structure:

## Section A — Required Denial Specification Table

| Dimension | Required State | Claim | Evidence | Confidence |
|----------|----------------|-------|----------|------------|
| Protectable Resource Form | | | | |
| Required Denial Decision Point | | | | |
| Required Denial Boundary | | | | |
| Required Actor / Authority | | | | |
| Required Denial Mode | | | | |
| Required Enforcement Requirement | | | | |
| Required Non-Compliance Consequence | | | | |
| Required Override Resistance | | | | |
| Required Visibility | | | | |
| Required Revalidation Requirement | | | | |

Immediately below the table, return this exact format:

**Required Actor Reachability Note**

Status: [Settled / Contested / Unknown]

Reasoning:
- [one to three sentences stating the basis for the reachability assessment, with reference to the boundary definition and any known constraints on the specified actor's authority]

Conditional requirement (if Contested or Unknown):
- [state what would need to be true — confirmed, reformed, or evidenced — before the required actor specification is reachable in practice]
- [optional second point]

## Section B — Required Denial Logic Statement

Return this exact format:

**Required Denial Logic Statement**

To protect [binding scarce resource] at the [binding level] level over the stated time horizon, denial must operate at or before [required denial decision point] by [required actor/authority] through [required denial mode], because allowing access beyond that point would expose the scarce resource to depletion, misallocation, or failed protection inconsistent with system stability.

## Section C — Failure-if-Absent Statement

Return this exact format:

**Failure-if-Absent Statement**

If this denial architecture does not exist in a binding form, the system is exposed to:
- [failure pathway 1]
- [failure pathway 2]
- [failure pathway 3]

## Section D — Evidence Register Pre-Population

At the end of Prompt 2, produce a pre-populated Evidence Register table.

Requirements:
- Include one row per mechanism category derived from the Required Denial Specification Table in Section A.
- Categories must be drawn from: denial decision point, denial actor/authority, denial mode, enforcement, consequence, override route, visibility, revalidation.
- Add three user-defined rows at the bottom.
- Maximum 15 rows total.
- Include the following columns for user completion: Evidence Type, Evidence Statement, Source.
- Evidence Type options: behavioural / structural / stress / explicit case fact.
- Evidence Statement rule: one sentence, factual, no interpretation, no causal language.
- Source rule: document name, observation, or interview reference only — no narrative.

Use this exact table structure:

| Item Number | Mechanism Category | Prompt 2 Reference | Evidence Type | Evidence Statement | Source |
|-------------|--------------------|--------------------|---------------|-------------------|--------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |
| 9 | | | | | |
| 10 | | | | | |
| 11 | User-defined | User-defined | | | |
| 12 | User-defined | User-defined | | | |
| 13 | User-defined | User-defined | | | |

End Section D with this exact instruction to the user:

*Complete the Evidence Register with your system-specific evidence. Leave unused rows blank. If you have no system-specific evidence, type SKIP. When complete, paste the completed register back into the chat.*

SKIP handling:
If the user types SKIP, before proceeding to Prompt 3, ask the user to select one of the following reason codes. Record the selected code in the Run Record under Evidence Register Status as: SKIP — [code]: [code description].

**SKIP Reason Codes:**
- **S1 — No relevant evidence available:** No field-validated or publicly available operational evidence has been identified for this system at this time.
- **S2 — Evidence exists but not yet gathered:** Evidence is likely to exist but has not been collected for this run; a field-informed rerun is anticipated.
- **S3 — Evidence exists but access is restricted:** Relevant evidence is known to exist but is not accessible to the analyst for this run.
- **S4 — Desktop run only — evidence not sought:** This run is intentionally structural and inferential; evidence gathering was not in scope.

The reason code selection must occur before ChatGPT proceeds past the Prompt 2 stop. It is not acceptable to proceed and record the reason code retrospectively in the Run Record.

When this Prompt 2 has successfully completed, stop and wait for either:
- SKIP, which triggers mandatory reason-code selection before Prompt 3 may be run, or
- a completed Evidence Register, which triggers the Validation Stage before Prompt 3.
```
---

## Validation Stage — Evidence Register Validation

### Purpose

Validate user-supplied system-specific evidence before it can enter Prompt 3.

This is a **named gating stage**, not a numbered prompt.

It fires only when the user pastes back a completed Evidence Register.

It does **not** fire if the user types **SKIP**.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DAI EXECUTION MODE here]

You are executing the Validation Stage of the Denial Architecture Interrogation (DAI).

Purpose:
Validate the user-submitted Evidence Register before any submitted item can be used in Prompt 3.

Trigger condition:
Run this stage only if the user has pasted back a completed Evidence Register. Do not run this stage if the user typed SKIP.

Use only:
- the completed Evidence Register submitted by the user
- the Scarcity Receipt Table
- the Boundary Lock Statement
- the Required Denial Specification Table

Do not perform any analytical assessment of the evidence.
Do not map actual denial architecture.
Do not infer causal meaning.
Do not reopen scarcity.

Process limit:
- The 15-item limit applies to the original Evidence Register submission only.
- If more than 15 items are submitted in the original register, process only the first 15 in submission order. Return all excess items with a note that the limit has been reached.
- Correction splits are amendments to existing items and do not count against the limit. The combined admitted register may therefore exceed 15 items after corrections.
- The 15-item limit cannot be circumvented by submitting composite items intended to be split through corrections. If this pattern is detected, the excess split items should be flagged.

For each submitted item, run these four exclusion tests:

Test 1 — Narrative contamination
Question: Does the Evidence Statement contain interpretive language such as suggests, indicates, shows that, because, therefore, this means?
Fail result: Requires Correction

Test 2 — Scope violation
Question: Does the item relate to a system layer, actor, or resource excluded in the SRIT boundary?
Fail result: Excluded — cannot be corrected

Test 3 — Scarcity reopening
Question: Does the item implicitly or explicitly challenge the Binding Scarce Resource Declaration?
Fail result: Excluded — cannot be corrected

Test 4 — Composite assertion
Question: Does the Evidence Statement contain more than one factual claim?
Fail result: Requires Correction — must be split into separate items

Validation rules:
- Items marked Requires Correction may be resubmitted.
- Maximum two correction rounds per item.
- If an item fails twice, it is automatically Excluded.
- Items marked Excluded are removed permanently. No resubmission permitted.
- The Validation Stage must produce no analytical assessment of the evidence.
- The Validation Stage must produce only pass/fail classifications with specific test references.

Output structure:

## Section A — Validation Results Table

| Item Number | Evidence Statement (abbreviated) | Test Result | Reason if not Admitted |
|-------------|----------------------------------|-------------|------------------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |
| 6 | | | |
| 7 | | | |
| 8 | | | |
| 9 | | | |
| 10 | | | |
| 11 | | | |
| 12 | | | |
| 13 | | | |
| 14 | | | |
| 15 | | | |

Allowed Test Result values:
- Admitted
- Requires Correction
- Excluded
- Withdrawn

## Section B — Excess Items Notice

If more than 15 items were submitted, return:

**Excess Items Notice**

Only the first 15 submitted items were processed. All additional items were ignored because the Validation Stage limit has been reached.

## Section C — Final Admitted Evidence Register

Only produce this section when all items are either Admitted, Excluded, or Withdrawn.

Return the final admitted items in this exact structure:

| Item Number | Mechanism Category | Prompt 2 Reference | Evidence Type | Evidence Statement | Source |
|-------------|--------------------|--------------------|---------------|-------------------|--------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |
| 9 | | | | | |
| 10 | | | | | |
| 11 | | | | | |
| 12 | | | | | |
| 13 | | | | | |
| 14 | | | | | |
| 15 | | | | | |

Then output this exact statement:

*Validation complete. [N] items admitted, [N] excluded, [N] withdrawn. Review the admitted items above. When you are ready to proceed, instruct Prompt 3.*

Correction handling:
- If any item is marked Requires Correction, stop after Section A and wait for the user to resubmit only the corrected items.
- Keep the existing item numbers.
- Apply the two-round maximum per item.
- If an item fails a second correction round, mark it Excluded automatically and do not allow further resubmission.
- Withdrawn: the user has indicated the item has no recoverable factual core and should be removed from the register. Mark all columns as WITHDRAWN in the corrections file. The Validation Stage will classify the item as Withdrawn. Withdrawn items are treated as Excluded for all downstream purposes and may not be resubmitted.

Correction submission format:
- Submit corrections as a separate corrections file containing only the corrected items.
- Do not resubmit the full register with corrections merged in.
- Use the original item number with a letter suffix for splits — for example 5a, 5b for an item 5 split into two.
- Mark withdrawn items explicitly with WITHDRAWN in all columns rather than omitting them.
- If a corrections file and the original register are both present, treat the original register as the baseline and the corrections file as amendments. Process only the corrected item numbers. Do not reprocess already-admitted items.
```

---

## Prompt 3 — Actual Denial Mapping

### Purpose

Map the denial architecture that actually operates in the live system.

This prompt identifies the **actual denial decision point** and actual mechanisms without yet making the final architecture judgement.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DAI EXECUTION MODE here]

You are executing Prompt 3 of the Denial Architecture Interrogation (DAI).

Purpose:
Map the denial architecture that actually operates in the live system.

Use only:
- the Scarcity Receipt Table
- the Boundary Lock Statement
- the Required Denial Specification Table
- the Admitted Evidence Register (if one was produced by the Validation Stage)
- any system facts already present in the prior analysis

Do not assess drift yet.
Do not judge alignment yet.
Do not upgrade inferred facts into evidence.

Task:
Identify the actual mechanisms by which the system currently restricts, delays, conditions, refuses, caps, escalates, or overrides access to the binding scarce resource.

For each actual mechanism, determine:
1. actual gate location
2. actual decision point
3. actual actor or authority
4. formality basis
5. operational denial mode
6. enforcement pattern
7. non-compliance consequence
8. known override route
9. evidence source
10. evidence status

Formality basis may include:
- formal written rule
- law or regulation
- board-approved policy
- operating procedure
- system-coded control
- budget or approval workflow
- contract
- custom or norm
- discretionary managerial practice
- political or informal influence

Evidence Source options may include:
- behavioural evidence
- structural evidence
- stress evidence
- explicit case fact
- inferred from system design
- unknown

Evidence Status options are:
- Confirmed
- Mixed
- Inferred
- Unknown

Evidence Status rules:

Confirmed:
The material content of the row is directly supported by admitted evidence and/or explicit case facts already present in the prior analysis. No material element of the row depends on unsupported inference.

Mixed:
The row contains at least one directly supported element, but one or more material elements remain inferred from structure, system design, or indirect indicators. Use Mixed when the mechanism is partially evidenced but not fully established.

Inferred:
The row is analytically plausible and Canon-consistent, but the material mechanism claim rests on system design logic, structural reasoning, or indirect indicators rather than direct admitted evidence or explicit case facts.

Unknown:
The current record cannot identify the mechanism, or a required material element of the mechanism, with defensible specificity. Do not infer a mechanism to fill the gap.

Source–Status interaction rules:
- Evidence Source and Evidence Status are separate fields and must not be conflated.
- Explicit case fact is an Evidence Source only. It must never be used as an Evidence Status.
- A row may list more than one Evidence Source where more than one source type applies.
- If a row includes admitted evidence but still depends on inference for one or more material elements, Evidence Status must be Mixed, not Confirmed.
- If the only defensible basis for a row is inferred from system design, Evidence Status must be Inferred.
- If no defensible basis exists to identify the mechanism, Evidence Source and Evidence Status should both be Unknown unless a narrower partial-source statement can be made without inventing facts.

Rules:
- Separate Confirmed and Mixed mechanisms from Inferred and Unknown mechanisms.
- If the system contains multiple denial mechanisms, map all material ones.
- If evidence is insufficient to identify an actual mechanism, do not invent one.
- If the Required Denial Specification identifies a mechanism type for which no evidence can be found in the current record, produce an explicit Unknown row in the Actual Denial Mapping Table with all fields set to Unknown and confidence set to Low. Do not omit the gap. Do not infer a mechanism to fill it. Unknown rows are valid analytical findings — they identify precisely where the actual architecture fails to match the required architecture.
- Admitted evidence items must be incorporated into the relevant rows of the Actual Denial Mapping Table by recording the applicable Evidence Source as explicit case fact and/or behavioural evidence, structural evidence, or stress evidence as appropriate.
- Assign Evidence Status separately using the four-status set above.
- Confidence must be rated on source quality and on the degree of unresolved inference remaining in the row.
- Do not draw inferences across admitted items.
- Do not synthesise narrative from admitted items.
- The number of mechanisms in the Actual Denial Mapping Table is not a quality indicator. Three well-grounded mechanisms with honest confidence ratings are more analytically valuable than eight mechanisms with inflated confidence. Do not add mechanisms to fill the table. Do not invent mechanisms to satisfy an expected count. Map only the mechanisms for which evidence exists.
- If too little information exists to map actual denial architecture meaningfully, halt with an Actual Denial Mapping Gap Notice.

Boundary conditions:
- **Gap Notice halt:** Use the Actual Denial Mapping Gap Notice only where the current record is too thin to produce a defensible Actual Denial Mapping Table and Summary at all. If the record cannot support a meaningful mapping, do not produce the mapping table or any threshold notice.
- **Warning threshold:** Apply only after a completed Actual Denial Mapping Table and Summary have been produced. Excluding the Unknown row for the required mechanism type if present, the warning threshold is met when 75% or more of mapped rows carry Evidence Status of Inferred or Unknown, and at least one mapped row remains more specific than a pure gap finding.
- **Critical threshold:** Apply only after a completed Actual Denial Mapping Table and Summary have been produced. The critical threshold is met when all mapped rows carry Evidence Status of Inferred or Unknown, including the required mechanism type row if present. This is a stronger near-threshold condition, not a replacement for the Gap Notice halt.

Use this halt format if needed:

**Actual Denial Mapping Gap Notice**

The current record is insufficient to map the actual denial architecture with defensible specificity.

Missing information:
- [item]
- [item]

Why this matters:
- [reason]

Minimum additional evidence needed:
- [evidence item]
- [evidence item]

Output structure:

## Section A — Actual Denial Mapping Table

| Mechanism | Actual Gate Location | Actual Decision Point | Actual Actor / Authority | Formality Basis | Operational Mode | Enforcement Pattern | Non-Compliance Consequence | Override Route | Evidence Source | Evidence Status | Confidence |
|----------|----------------------|-----------------------|--------------------------|----------------|------------------|---------------------|----------------------------|----------------|-----------------|----------------|------------|

## Section B — Actual Denial Mapping Summary

Return:

**Actual Denial Mapping Summary**

Material denial mechanisms identified:
1. [mechanism]
2. [mechanism]
3. [mechanism]

Most binding current mechanism:
- [text]

Most uncertain mechanism:
- [text]

Primary evidence weakness:
- [text]

Near-threshold evidence check:
After producing the Actual Denial Mapping Summary, count the Evidence Status distribution across all mapped rows, excluding the Unknown row for the required mechanism type if present.

If the warning threshold is met but the critical threshold is not met, produce this notice and then stop:

**Near-Threshold Evidence Notice**

The Actual Denial Mapping is predominantly inferred. [X] of [Y] mapped rows carry Inferred or Unknown Evidence Status (Y excludes the Unknown row for the required mechanism type if present). The current record is sufficient to proceed, but the denial architecture assessment will carry materially reduced confidence and is likely to result in Qualified Ready at Prompt 5 Stage 1.

Before proceeding to Prompt 4, the user may:
- **CONTINUE:** Accept the inferred mapping and proceed to Prompt 4.
- **PAUSE:** Return to evidence admission before the mapping closes.

State exactly:
Type CONTINUE to proceed to Prompt 4, or PAUSE to return to evidence admission before the mapping closes.

If the critical threshold is met, produce this escalated notice and then stop:

**Critical Near-Threshold Evidence Notice**

The Actual Denial Mapping is entirely inferred or unknown. [X] of [Y] mapped rows carry Inferred or Unknown Evidence Status (Y includes all mapped rows, including the required mechanism type row if present). The mapping is sufficient to continue, but the denial architecture assessment may be insufficient to support an unqualified readiness outcome and may result in Not Ready at Prompt 5 Stage 1.

Before proceeding to Prompt 4, the user may:
- **CONTINUE:** Accept the inferred mapping and proceed to Prompt 4.
- **PAUSE:** Return to evidence admission before the mapping closes.

State exactly:
Type CONTINUE to proceed to Prompt 4, or PAUSE to return to evidence admission before the mapping closes.

PAUSE re-entry sequence:
PAUSE invoked → evidence admission pathway → Validation Stage if triggered → full Prompt 3 rerun from scratch.

Resume mid-output is not permitted. If new evidence is admitted after PAUSE, Prompt 3 must be rerun in full because the row set, row classifications, evidence distribution, mapping summary, and threshold outcome may all change.

If neither threshold is met, when this Prompt 3 has successfully completed, stop and wait for explicit instruction before proceeding to Prompt 4.
```
---

## Prompt 4 — Authority, Enforcement, and Override Analysis

### Purpose

Determine whether the mapped denial mechanisms are genuinely binding by testing authority source, enforcement strength, non-compliance consequences, override permeability, visibility, and durability.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DAI EXECUTION MODE here]

You are executing Prompt 4 of the Denial Architecture Interrogation (DAI).

Purpose:
Determine whether the mapped denial mechanisms are genuinely binding by testing authority source, enforcement strength, non-compliance consequences, and override permeability.

Use only:
- the Actual Denial Mapping Table
- the Actual Denial Mapping Summary
- the Required Denial Specification Table
- the Required Actor Reachability Note

Do not perform drift classification yet.
Do not perform final denial architecture judgement yet.

Task:
For each mapped denial mechanism, assess the following:

1. authority basis
2. authority strength
3. enforcement status
4. consequence severity
5. override permeability
6. visibility
7. revalidation durability
8. practical binding force

Authority basis categories:
- legal / regulatory
- constitutional / mandate-based
- board / governance
- policy / procedure
- contractual
- budgetary / approval-rights
- technical / system-enforced
- operational / workflow
- normative / cultural
- informal / political / personal

Authority strength scale:
- weak
- moderate
- strong
- dominant

Enforcement status:
- absent
- symbolic
- discretionary
- selectively applied
- consistently applied
- automatically enforced
- coercively enforced

Consequence severity:
- none
- reputational only
- soft escalation
- work refusal / stop-go
- economic penalty
- formal sanction
- exclusion / shutdown

Override permeability:
- open
- high
- moderate
- low
- near-closed

Visibility:
- hidden
- low visibility
- visible to operators only
- visible to managers
- system-wide visible
- externally visible

Revalidation durability:
- none
- ad hoc
- periodic informal
- periodic formal
- event-triggered formal
- continuous

Practical binding force:
- non-binding
- weakly binding
- conditionally binding
- strongly binding
- decisively binding

Rules:
- A denial mechanism may be formal but weak.
- A denial mechanism may be informal but strongly binding.
- A written rule with no consequence should not be treated as robust denial.
- A mechanism that can be routinely bypassed should be downgraded even if formal.
- Unknown rows inherited from Prompt 3 must be carried into the Denial Authority Matrix with authority basis set to not evidenced, enforcement status set to absent, and practical binding force set to non-binding. Do not infer or fabricate authority for Unknown mechanisms. Record the same Unknown origin in the Claim column.
- Every row must contain Claim → Evidence → Confidence.

Output structure:

## Section A — Denial Authority Matrix

| Mechanism | Authority Basis | Authority Strength | Enforcement Status | Consequence Severity | Override Permeability | Visibility | Revalidation Durability | Practical Binding Force | Claim | Evidence | Confidence |
|----------|------------------|--------------------|--------------------|----------------------|-----------------------|-----------|-------------------------|------------------------|-------|----------|------------|

## Section B — Binding Reality Summary

Return this exact format:

**Binding Reality Summary**

Mechanisms that are genuinely binding in practice:
- [mechanism]
- [mechanism]

Mechanisms that are formal but weak:
- [mechanism]
- [mechanism]

Mechanisms that are primarily symbolic:
- [mechanism]
- [mechanism]

Most important override vulnerability:
- [text]

Most important authority weakness:
- [text]

When this Prompt 4 has successfully completed, stop and wait for explicit instruction before proceeding to Prompt 5.
```

---

## Prompt 5 — Denial Architecture Judgement

### Purpose

Make a structured judgement about whether the actual denial architecture exists in a form capable of protecting the binding scarce resource.

This completes DAI and creates the handoff point into Drift Detection Analysis.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DAI EXECUTION MODE here]

You are executing Prompt 5 of the Denial Architecture Interrogation (DAI).

Purpose:
Make a structured judgement about whether the actual denial architecture exists in a form capable of protecting the binding scarce resource.

Use only:
- the Scarcity Receipt Table
- the Required Denial Specification Table
- the Required Actor Reachability Note
- the Actual Denial Mapping Table
- the Denial Authority Matrix
- the Binding Reality Summary

Do not perform drift classification yet.
Do not perform system risk classification yet.

Task:
Compare the required denial architecture with the actual denial architecture and determine whether the system currently possesses a denial architecture that is real, binding, and potentially capable of protecting the scarce resource.

Assess the actual denial architecture against these dimensions:
1. correct resource targeted
2. correct level
3. correct decision point
4. authority adequacy
5. enforcement adequacy
6. consequence adequacy
7. override resistance
8. visibility
9. revalidation durability

Then assign one overall Denial Architecture Status:

- aligned and binding
- aligned but fragile
- partially aligned
- mislocated
- symbolic
- absent

Rules:
- “Aligned and binding” requires more than formal existence.
- “Symbolic” applies where nominal denial exists but practical binding force is weak.
- “Mislocated” applies where denial exists but sits too far downstream, too far upstream, or on the wrong layer.
- “Absent” applies where no credible denial mechanism can be identified.
- Provide one strongest counter-interpretation and explain why it is weaker.
- Every conclusion must follow Claim → Evidence → Confidence.
- If the Required Actor Reachability Note is Contested or Unknown, include at least one DAI-generated authority-basis test question in Section E.

Output structure:

## Section A — Denial Architecture Comparison Table

Variance scale for the Comparison Table:
— None: actual state matches required state
— Low: minor gap; actual state is close to required state
— Low-Moderate: partial gap; actual state meets some but not all requirements
— Moderate: material gap; actual state partially addresses the dimension but with meaningful shortfall
— High: severe gap; actual state is materially below required state
— Critical: unmitigated failure; the dimension represents a direct architectural failure that cannot be compensated by other dimensions

| Dimension | Required State | Actual State | Variance | Claim | Evidence | Confidence |
|----------|----------------|-------------|----------|-------|----------|------------|

## Section B — Denial Architecture Judgement

Return this exact format:

**Denial Architecture Judgement**

For [system], the current denial architecture protecting [binding scarce resource] is assessed as **[status]**.

Why:
- [reason]
- [reason]
- [reason]

Primary weakness:
- [text]

Primary strength:
- [text]

## Section C — Strongest Counter-Interpretation

Return:

**Strongest Counter-Interpretation**

Alternative reading:
- [text]

Why it is weaker:
- [reason]
- [reason]

## Section D — Readiness for Drift Analysis

Return this exact format:

**Readiness for Drift Analysis**

Assign one of three statuses:

**Ready** — the judgement is sound, the evidence base is sufficient to support the Denial Architecture Status assigned, and DDA may proceed without qualification. Apply where at least some Evidence Register data has been admitted, or where the Actual Denial Mapping produces a predominantly Confirmed or Mixed Evidence Status across Prompt 3 rows.

**Qualified Ready** — the judgement is analytically sound and Canon-consistent, but the evidence base is predominantly Inferred or Unknown and no Evidence Register data was admitted at the Prompt 2 stop. DDA may proceed. Attach the following qualification notice to the readiness output, and instruct the user to carry it into the DDA ChatGPT session for attachment to all DDA findings:

"This analysis was conducted on a predominantly inferred evidence base. Findings are Canon-grounded and analytically defensible but carry reduced confidence. A field-informed rerun with admitted Evidence Register data is required before findings are treated as operationally validated."

**Not Ready** — reserved for runs where the Prompt 3 evidence base is too thin to map actual denial architecture meaningfully — i.e. where the Actual Denial Mapping Gap Notice threshold would have been reached. DDA cannot proceed until DAI is rerun with Evidence Register data.

Trigger logic for status assignment:

For this readiness test, "predominantly" means more than half of mapped rows carry the relevant grouped Evidence Status, excluding the Unknown row for the required mechanism type if present.

| Condition | Status |
|-----------|--------|
| Evidence Register data admitted AND judgement sound | Ready |
| No Evidence Register data admitted AND Prompt 3 evidence predominantly Inferred or Unknown AND judgement sound | Qualified Ready |
| Evidence base too thin to map actual denial architecture | Not Ready |

Then return:

Status: [Ready / Qualified Ready / Not Ready]

Reason:
- [one line]

Qualification notice (Qualified Ready only):
- [reproduce the fixed notice verbatim]

If not ready, missing requirement:
- [text]

## Section E — Authority-Basis Test Questions [DAI-generated]

Return this exact format:

**Authority-Basis Test Questions [DAI-generated]**

If the Required Actor Reachability Note status is Settled:
- None — reachability is settled on the current record.

If the Required Actor Reachability Note status is Contested or Unknown:
- [question specifically testing the authority basis of the required actor]
- [optional second question]

**Prompt 5 — Stage 1 complete.**

When this Prompt 5 Stage 1 has successfully completed, stop. Do not produce the Run Record yet. The Denial Architecture Interrogation module analytical output is complete. Wait for the explicit instruction: **Execute Run Record** to proceed to Stage 2.
```

---

## DAI Run Record Integration

### Purpose

Capture the full output of the Denial Architecture Interrogation (DAI) in a single downstream artefact that can be used as the fixed analytical input to Drift Detection Analysis (DDA).

The DAI Run Record should preserve:

- the upstream scarcity inheritance from SRIT
- the locked denial-analysis boundary
- the required denial architecture
- the actual denial architecture
- the authority and enforcement assessment
- the final denial architecture judgement
- explicit readiness status for Drift Detection Analysis
- any qualification notice required for downstream DDA
- the Prompt 2 reachability finding and any DAI-generated authority-basis test questions

The DAI Run Record is produced only after DAI Prompt 5 has completed.

If DAI Prompt 5 returns **Readiness for Drift Analysis: Not Ready**, the run record may still be saved, but DDA must not be executed until the missing requirement has been resolved.

### Prompt 5 — Stage 2: Run Conclusion and DAI Run Record

This section executes only when the user instructs: **Execute Run Record**.

Do not say "let me produce the Run Record", "I will now generate", or any similar preamble. Output the conclusion statement and Run Record directly in response to that instruction. Deliver the Run Record inside a fenced code block using triple backticks. Do not render the Run Record as formatted markdown.

**Conclusion statement:**

> This DAI analysis is now complete. The Denial Architecture Judgement and supporting artefacts are ready for downstream Drift Detection Analysis if the Readiness for Drift Analysis status is Ready or Qualified Ready. If the status is Qualified Ready, carry the qualification notice below into the DDA ChatGPT session and attach it to all DDA findings. Save the DAI Run Record below as:
>
> `DAI_Run_[SystemName]_[YYYY-MM-DD_HHMM].md`
>
> where [SystemName] is the system name from the System Definition Statement and [YYYY-MM-DD_HHMM] is the date and time of this run.

**DAI Run Record — output immediately below the conclusion statement:**

```markdown
# DAI Run Record

## Run Metadata
- **System:** [system name]
- **Run Date/Time:** [YYYY-MM-DD HH:MM]
- **AI Model:** [model name and version]
- **Thinking Mode:** [Standard / Extended / Not applicable]
- **DAI Version:** 1.7

---

## DAI Input Rule
- **Permitted upstream inputs:** SRIT Run Record and the Evidence Register created and populated during the current DAI run only.
- **Prior DAI evidence reuse:** No evidence from a prior DAI run may be admitted unless it is re-admitted through the current run's Evidence Register and current Validation Stage.

---

## Upstream SRIT Reference
- **Source File:** [SRIT filename if known]
- **SRIT Version:** [version if known]

---

## System Definition Statement
[Reproduce the full System Definition Statement from the SRIT Run Record]

---

## Binding Scarcity Declaration
[Reproduce the exact Binding Scarcity Declaration from the SRIT Run Record]

**Selection Rationale**
[Reproduce the SRIT Selection Rationale in full]

---

## Strongest Alternative Rejected
[Reproduce the strongest alternative candidate and rejection rationale from the SRIT Run Record]

---

## Confidence Rating and Residual Uncertainty
[Reproduce the SRIT Confidence Rating and Residual Uncertainty section in full]

---

## DAI Entry Test Questions
[Reproduce the DAI Entry Test Questions carried forward from SRIT]

---

## Scarcity Receipt Table
[Reproduce Prompt 1 Section A in full]

---

## Boundary Lock Statement
[Reproduce Prompt 1 Section B in full]

---

## Required Denial Specification Table
[Reproduce Prompt 2 Section A in full]

---

## Reachability Finding
[Reproduce the Required Actor Reachability Note in full]

---

## Required Denial Logic Statement
[Reproduce Prompt 2 Section B in full]

---

## Failure-if-Absent Statement
[Reproduce Prompt 2 Section C in full]

---

## Evidence Register Status
- **Prompt 2 Evidence Register Produced:** [Yes / No]
- **Validation Stage Invoked:** [Yes / No]
- **Validation Outcome:** [Skipped / Completed / Incomplete]
- **SKIP Reason Code:** [None / SKIP — S1: No relevant evidence available / SKIP — S2: Evidence exists but not yet gathered / SKIP — S3: Evidence exists but access is restricted / SKIP — S4: Desktop run only — evidence not sought]

---

## Final Admitted Evidence Register
[If a Validation Stage produced a Final Admitted Evidence Register, reproduce it in full. If SKIP was used or no items were admitted, state: No admitted evidence register produced.]

---

## Actual Denial Mapping Table
[Reproduce Prompt 3 Section A in full]

---

## Actual Denial Mapping Summary
[Reproduce Prompt 3 Section B in full]

---

## Denial Authority Matrix
[Reproduce Prompt 4 Section A in full]

---

## Binding Reality Summary
[Reproduce Prompt 4 Section B in full]

---

## Denial Architecture Comparison Table
[Reproduce Prompt 5 Section A in full including the variance ratings]

---

## Denial Architecture Judgement
[Reproduce Prompt 5 Section B in full]

---

## Strongest Counter-Interpretation
[Reproduce Prompt 5 Section C in full]

---

## Readiness for Drift Analysis
[Reproduce Prompt 5 Section D in full]

---

## Qualification Notice
[If Status is Qualified Ready, reproduce the fixed qualification notice verbatim. Otherwise state: None.]

---

## Authority-Basis Test Questions [DAI-generated]
[Reproduce Prompt 5 Section E in full]

---
```

### DDA Input Rule

Drift Detection Analysis should use the DAI Run Record as its primary upstream artefact.

At minimum, DDA must be able to recover from the DAI Run Record:

- the locked system boundary
- the Binding Scarce Resource Declaration
- the Required Denial Specification Table
- the Reachability Finding
- the Actual Denial Mapping Table
- the Denial Authority Matrix
- the Denial Architecture Comparison Table
- the Denial Architecture Judgement
- the Readiness for Drift Analysis status
- the Qualification Notice where Status is Qualified Ready
- the Authority-Basis Test Questions [DAI-generated]

If the Readiness for Drift Analysis status is **Qualified Ready**, DDA may proceed but must attach the Qualification Notice to all DDA findings.

If the Readiness for Drift Analysis status is **Not Ready**, DDA must halt and report the missing requirement rather than proceed.

---

## Build Notes

### Current execution mode

This file is built for **single-prompt testing**.

That means the model should:

- execute only the prompt or named stage explicitly invoked
- stop at the end of that prompt or named stage
- preserve all structured artefacts for the next run

### Validation logic

The Validation Stage exists to allow user-supplied system evidence to enter the protocol **without contaminating analytical discipline**.

It admits only evidence that is:

- non-narrative
- within boundary
- non-reopening of scarcity
- atomised into single factual claims

### Future conversion

Once the prompt set is validated, this file can be converted into:

- a continuous-run DAI script
- a DAI run record template
- a downstream Drift Detection Analysis prompt set

---

## File Naming Convention

Recommended filename for distribution and storage:

`DAI_Prompts_v1_7.md`
