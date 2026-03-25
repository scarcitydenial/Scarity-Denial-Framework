# SRIT — Claude Review

*Version 0.3.4 — uploadable instruction file — companion to SRIT v1.8*

---

## Preamble

This file is an instruction document for the Claude companion session. Claude should read it in full and execute the instructions below. The user has uploaded this file after receiving the SRIT Prompt 6 Stage 1 output from ChatGPT.

---

## Claude Instructions

### 1. Receive the Stage 1 output

Ask the user to paste the SRIT Prompt 6 Stage 1 output from ChatGPT into this session.

Do not proceed until it is received.

### 2. Review the declaration against the Canon

Assess the Stage 1 output against the Scarcity–Denial Canon. Identify any concerns with:

- Whether the declared resource is a resource or a mechanism — apply the Canon's second sentence as the test: if the candidate governs the deployment of other resources rather than being the resource itself, it is a mechanism, not a scarce resource
- Whether the selection rationale is grounded in the candidate evidence or in narrative coherence
- Whether the strongest alternative rejected is genuinely addressed or dismissed without substantive reasoning
- Whether the confidence rating is consistent with the analytical basis presented — a declaration where multiple candidates remain plausible after elimination, or where the selection rationale relies on structural argument rather than observable system behaviour, should carry a confidence rating of 7 or below
- **Adversarial challenge record adequacy** — For each candidate eliminated under R6 at Prompt 4, confirm that an adversarial challenge record is present in the Run Record containing: a challenge argument, a counter-argument, and a disposition statement. Assess whether the counter-argument is specifically grounded in the Canon's second sentence — it must identify what governs what, and demonstrate that the candidate's failure pathway runs through mobilisation or governance of another resource rather than through direct depletion. A counter-argument that simply restates the elimination conclusion without demonstrating the mechanism/resource distinction is inadequate. If any R6 elimination is missing its challenge record, or if any counter-argument is not grounded in the Canon's second sentence, state this as a concern requiring resolution before Stage 2 is instructed.
- **Protectable resource form adequacy** — Confirm that the declaration includes a Protectable Resource Form field (Prompt 6 Section B) and that it meets the following standard: it specifies what must be preserved, in what operational state, at what level, and what substitution would fail to replace it under the declared failure condition. An adequate protectable resource form statement is operationally specific — it distinguishes the resource as it must exist to be protective from abstract or nominal forms that may exist without providing protection. If the Protectable Resource Form field is absent, state this as a concern requiring resolution before Stage 2 is instructed. If the field is present but insufficiently specific — for example, if it merely restates the resource name without operational precision — state this as a concern and specify what additional precision is needed. If the field is present and adequate, confirm it and note that it will pre-populate the DAI Prompt 2 Required Denial Specification Table Protectable Resource Form row, reducing re-derivation at DAI.
- Whether the Stage 1 Test Questions are specific enough to serve as the opening questions for DAI analysis

### 3. State your assessment

State any concerns clearly with specific reference to the output. If there are no concerns, confirm the declaration is ready for Run Record production.

If concerns are present, specify exactly what needs to be resolved in ChatGPT before Stage 2 is instructed.

### 4. When the declaration is confirmed ready — receive the Run Record

Once the user has resolved any concerns and instructed ChatGPT Stage 2, ask them to paste the Run Record code block from ChatGPT into this session.

Do not produce the Run Record file until the code block is received.

### 5. Produce the named Run Record file

Ask the user for their local time.

Format the Run Record into clean markdown and produce the correctly named file:

`SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Where SystemName is taken from the System Definition Statement in the Run Record and HHmm is the local time provided by the user.

### 6. Produce the Module Commentary Summary

Produce a compact structured summary of the key observations made during the SRIT run commentary. Include the following sections:

**Declaration and confidence rating** — state the declared resource and confidence rating

**Strongest alternative rejected** — state it and why it was set aside

**Adjacent system signals** — list any identified, or state none

**Residual uncertainties** — list any that should be carried into DAI

**Carry-forward recommendations made** — list each recommendation made to ChatGPT during the run, the prompt it related to, and whether ChatGPT acted on it, partially acted on it, or did not act on it

**Unacted recommendations** — list any carry-forward recommendations that ChatGPT did not act upon, with the specific concern and the prompt at which it was raised. If all recommendations were acted upon, or no recommendations were made, state: *No unacted recommendations.*

**Prompts where concerns were raised** — note any prompts where concerns were identified and how they were resolved

Name the file:

`SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Use the same SystemName and time as the Run Record.

---

## Claude Output Format

Produce outputs in this sequence:

1. Declaration assessment — concerns or confirmation of readiness
2. *(After Stage 2 and Run Record receipt)* The formatted Run Record file
3. The Module Commentary Summary file

---

## User Next Step

Save both files produced by Claude:
- `SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Upload `DAI_Claude_BoundaryCheck_v0_3_3.md` to this Claude session to begin the SRIT → DAI boundary check.

Do not open a new Claude session.

---

*Version 0.3.4 — companion to SRIT v1.8*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0. No derivative works without prior written approval.*
