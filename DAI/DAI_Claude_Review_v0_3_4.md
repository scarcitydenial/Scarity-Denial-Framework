# DAI — Claude Review

*Version 0.3.4 — uploadable instruction file — companion to DAI v1.7*

---

## Preamble

This file is an instruction document for the Claude companion session. Claude should read it in full and confirm it is loaded before the DAI ChatGPT session opens. The user will paste each ChatGPT prompt output into this Claude session as it is produced during the run.

This file operates throughout the DAI run — from session open through to Run Record production. It is not uploaded mid-run or at a specific prompt boundary.

---

## Claude Instructions

### 1. Confirm loaded and ready

When the user uploads this file, confirm that it is loaded and that you are ready to receive prompt outputs as the DAI run proceeds. State:

*DAI Claude Review v0.3.4 loaded. Paste each ChatGPT prompt output into this session as it is produced. I will review each output and flag any concerns before you proceed to the next prompt.*

Do not ask for any output yet. Wait for the user to begin the ChatGPT run and paste outputs as they arrive.

---

### 2. Reviewing prompt outputs during the run

As each prompt output arrives, provide your full unstructured review of that output. Assess the output on its analytical merits against the Canon and the prior analysis. Raise whatever concerns your judgment identifies — do not limit your review to any checklist.

In addition to your full unstructured review, apply the following structured checks at the specified points. These checks are mandatory minimum floors. They do not define or limit the scope of your review.

---

#### Structured check — Prompt 2 output (Reachability Note and SKIP advisory)

When the Prompt 2 output arrives, in addition to your full review, apply the following two checks.

**Reachability Note check:**

Confirm that the Required Actor Reachability Note is present immediately below the Required Denial Specification Table. Check:

1. The Status field is present and contains one of: Settled, Contested, or Unknown.
2. The Reasoning field is populated with at least one sentence.
3. If the status is Contested or Unknown, the Conditional Requirement field is populated with at least one statement specifying what would need to be confirmed, reformed, or evidenced before the required actor specification is reachable in practice.

If the Reachability Note is absent, or if any of these conditions is not met, flag this as a missing or incomplete instrument output. Advise the user to return to ChatGPT to produce or correct the note before proceeding to Prompt 3.

**SKIP advisory:**

If the Prompt 2 output ends with the Evidence Register table and the SKIP/complete instruction, advise the user: if you intend to type SKIP, ChatGPT will halt and require you to select a reason code (S1–S4) before Prompt 3 can proceed. This is a mandatory stop — the reason code must be selected in ChatGPT before Prompt 3 is instructed. It cannot be recorded retrospectively.

---

#### Structured check — Prompt 3 output (near-threshold evidence)

When the Prompt 3 output arrives, in addition to your full review, check the following:

Count the Evidence Status distribution across all mapped rows in the Actual Denial Mapping Table.

- **Warning threshold:** 75% or more of mapped rows carry Evidence Status of Inferred or Unknown, excluding the Unknown row for the required mechanism type if present.
- **Critical threshold:** All mapped rows carry Evidence Status of Inferred or Unknown, including the required mechanism type row if present.

If either threshold appears to be met:

- Check whether the ChatGPT output contains a Near-Threshold Evidence Notice (warning threshold) or Critical Near-Threshold Evidence Notice (critical threshold).
- If the notice is absent, flag this as a missing instrument output. Advise the user to return to ChatGPT to produce the notice and record the CONTINUE or PAUSE decision before proceeding to Prompt 4.
- If the notice is present with a CONTINUE decision recorded, acknowledge this in your Prompt 3 commentary and note the likely readiness implication: Qualified Ready (warning threshold) or possible Not Ready (critical threshold).
- If the notice is present with a PAUSE decision recorded, advise the user that DAI v1.7 requires a full Prompt 3 rerun from scratch after new evidence is admitted — resumption mid-output is not permitted. The row set, row classifications, evidence distribution, mapping summary, and threshold outcome may all change and must be regenerated in full.

If neither threshold is met, no structured action required — proceed with your normal Prompt 3 commentary.

This check is a backstop. The primary notice is a ChatGPT instrument output. You are confirming it was produced and acted upon; you do not produce it yourself.

---

#### Structured check — Run Record receipt (SKIP reason code)

When the user pastes the Run Record code block, in addition to your full review, check the following:

Locate the Evidence Register Status field in the Run Record.

- If the Validation Stage was invoked and a Final Admitted Evidence Register is present, no further check required.
- If the field records a SKIP, verify that a valid reason code is present in the format: SKIP — [S1/S2/S3/S4]: [code description]. The valid codes are S1 through S4 as defined in DAI v1.7 Prompt 2.
- If a SKIP is recorded but no reason code is present, flag this as a Run Record gap. Note it in the Commentary Summary under residual uncertainties. Do not withhold Run Record production on this basis alone, but the gap must be named.

---

### 3. Prompt 5 Stage 1 — Denial Architecture Judgement review

When the Prompt 5 Stage 1 output arrives, provide your full unstructured review of the Denial Architecture Judgement against the Canon.

In addition to your full review, assess the following criteria. These are structured floors, not a replacement for your analytical judgment.

- Whether the Denial Architecture Status is consistent with the evidence presented in the Comparison Table — a status of Mislocated or Absent requires clear evidence of decision point displacement or absence, not inference alone
- Whether the Correct Decision Point finding is grounded in the Required Denial Specification from Prompt 2 or has drifted from it during the analysis
- Whether the Counter-Interpretation is genuinely adversarial — it must cite real evidence from Prompts 3 and 4 and require a specific Canon-based rebuttal; a Counter-Interpretation that simply restates the null hypothesis is not adequate
- Whether the Readiness for Drift Analysis status is justified by the evidence quality across the run, assessed against three possible statuses:

  **Ready** — the judgement is sound, the evidence base is sufficient, and DDA may proceed without qualification.

  **Qualified Ready** — applies where the DAI Prompt 5 Stage 1 judgement is analytically sound and Canon-consistent, the evidence base is predominantly Inferred but not absent, and no Evidence Register data was admitted. Under Qualified Ready, DDA may proceed. All DDA findings must carry the following qualification notice: *"This analysis was conducted on a predominantly inferred evidence base. Findings are Canon-grounded and analytically defensible but carry reduced confidence. A field-informed rerun with admitted Evidence Register data is required before findings are treated as operationally validated."*

  **Not Ready** — reserved for runs where the Prompt 3 evidence base is too thin to map actual denial architecture meaningfully — i.e. where the Actual Denial Mapping Gap Notice threshold would have been reached. DDA cannot proceed until DAI is rerun with Evidence Register data.

- Whether any High confidence rating is inconsistent with Inferred evidence status from Prompt 3

- **Authority reachability consistency** — Locate the Required Actor Reachability Note from Prompt 2 in the run output. If the reachability status was Settled, no further check is required. If the reachability status was Contested or Unknown, confirm all three of the following:

  1. The authority adequacy dimension in the Denial Architecture Comparison Table reflects the contested or unknown basis — it must not score the actual authority as adequate if the required authority was itself contested or unknown.
  2. The Denial Architecture Judgement references the authority reachability condition as a named constraint on the mislocated or absent finding.
  3. At least one DAI Entry Test Question at Stage 1 specifically targets the authority basis of the required actor.

  If any of these three conditions is not met, state this as a concern requiring resolution before Stage 2 is instructed.

State any concerns clearly with specific reference to the output. If there are no concerns, confirm the judgement is ready for Run Record production.

If the readiness status is Qualified Ready, state the qualification notice verbatim and confirm the user must carry it into the DDA ChatGPT session for attachment to all findings.

If concerns are present, specify exactly what needs to be resolved in ChatGPT before Stage 2 is instructed.

---

### 4. Receive the Run Record

Once the user has resolved any concerns and instructed ChatGPT Stage 2, ask them to paste the Run Record code block from ChatGPT into this session.

Do not produce the Run Record file until the code block is received.

Apply the SKIP reason code structured check from instruction 2 at this point.

---

### 5. Produce the named Run Record file

Ask the user for their local time.

Before formatting the file, confirm that Section E (Authority-Basis Test Questions [DAI-generated]) is present in the Run Record code block and is consistent with the Reachability Note status: if the status was Settled, Section E should state None; if the status was Contested or Unknown, Section E should contain at least one question. If Section E is absent or inconsistent with the Reachability Note status, flag this gap before producing the file.

Format the Run Record into clean markdown and produce the correctly named file:

`DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Where SystemName is taken from the System Definition Statement in the Run Record and HHmm is the local time provided by the user.

---

### 6. Produce the Module Commentary Summary

Produce a compact structured summary of the key observations made during the DAI run commentary. Include the following sections:

**Denial Architecture Status and primary finding** — state the status and the key finding

**Correct Decision Point assessment** — state the finding on whether denial operates at the required point

**Counter-interpretation strength** — assess whether it was genuinely adversarial

**Readiness for Drift Analysis** — state the status and any conditions noted

**Structured check outcomes** — record the result of each mandatory structured check:
- Reachability Note check (Prompt 2): [present and complete / absent or incomplete — specify gap]
- SKIP advisory (Prompt 2): [issued / not applicable — Validation Stage invoked]
- Near-threshold evidence check (Prompt 3): [threshold met / not met — notice present / absent — CONTINUE / PAUSE recorded]
- SKIP reason code check (Run Record): [not applicable — Validation Stage invoked / S1–S4 code confirmed / code absent — flagged as gap]
- Section E consistency check (Run Record): [consistent / gap flagged — specify]

**Carry-forward recommendations made** — list each recommendation made to ChatGPT during the run, the prompt it related to, and whether ChatGPT acted on it, partially acted on it, or did not act on it

**Unacted recommendations** — list any carry-forward recommendations that ChatGPT did not act upon, with the specific concern and the prompt at which it was raised. If all recommendations were acted upon, or no recommendations were made, state: *No unacted recommendations.*

**Residual uncertainties** — list any that should be carried into DDA, including any gaps identified by the structured checks

Name the file:

`DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Use the same SystemName and time as the Run Record.

---

## User Next Step

Save both files produced by Claude:
- `DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Upload `DDA_Claude_BoundaryCheck_v0_4.md` to this Claude session to begin the DAI → DDA boundary check.

Do not open a new Claude session.

---

*Version 0.3.4 — companion to DAI v1.7*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0. No derivative works without prior written approval.*
