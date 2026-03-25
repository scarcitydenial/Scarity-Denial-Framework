# Scarcity–Denial Framework — Runtime Guide

*Version 0.5.2*

\---

## Purpose

This document sequences a complete three-module pipeline run from first session to final artefact. It sits above the nine module operational documents — those tell you how to operate each individual session; this document tells you the overall flow, what to carry between sessions, and what decisions to make at each module boundary.

Read this document before beginning any run. Keep it open alongside the module operational documents during the run.

\---

## The Two-Platform Architecture

Every run uses two platforms operating in parallel throughout:

**Claude Sonnet 4.6** — one session, opened before the run begins, kept open for the entire three-module run. Handles system description preparation, active commentary on every ChatGPT prompt output, Stage 1 review at each module boundary, Run Record formatting and naming at each module close, and Module Commentary Summary production.

**ChatGPT GPT-5.4 Thinking Extended** — three separate sessions, one per module. Handles analytical execution only.

\---

## How the Two Platforms Are Instructed

The two platforms require different instruction methods by design. This is intentional, not an inconsistency.

### Claude — uploadable instruction files

Claude-facing documents are uploaded directly to the Claude companion session. Claude reads and executes them. The user does not need to interpret these documents — Claude manages the step and tells the user what to do next.

After reviewing each prompt output, Claude will either provide commentary only, or commentary plus a **carry-forward note** — a reasoned recommendation for ChatGPT's consideration before the next prompt fires. Carry-forward notes are recommendations, not overrides. ChatGPT may accept them, partially accept them, or proceed without acting on them. Any recommendation that ChatGPT does not act upon will be recorded in the Unacted Recommendations section of the Module Commentary Summary.

Documents used this way, in run order:

* `SRIT_Claude_SysDesc_v0_4_4.md` — uploaded to open the session and initialise the full run
* `SRIT_Claude_Review_v0_3_4.md` — uploaded after SRIT ChatGPT Prompt 6 Stage 1
* `DAI_Claude_BoundaryCheck_v0_3_3.md` — uploaded at the SRIT → DAI boundary
* `DAI_Claude_Review_v0_3_4.md` — uploaded at the SRIT → DAI boundary, immediately after the Boundary Check confirms Ready, before the DAI ChatGPT session opens
* `DAI_Evidence_Register_v0_2.md` — uploaded at DAI Prompt 2 stop (if evidence available)
* `DDA_Claude_BoundaryCheck_v0_4.md` — uploaded at the DAI → DDA boundary
* `DDA_Claude_Review_v0_4.md` — uploaded after DDA ChatGPT Prompt 5 Stage 1

### ChatGPT — drag-and-drop files plus copy-paste opening instruction

ChatGPT-facing documents use a two-part approach:

**Drag and drop** — the Canon and Prompt architecture files are dragged into the ChatGPT session as document context. ChatGPT reads them as the governing framework and execution protocol.

**Copy-paste opening instruction** — each ChatGPT RunSetup document contains an opening instruction block that must be pasted as direct user text. This is intentional. The opening instruction establishes the behavioural constraints, model and thinking mode requests, and session framing before ChatGPT begins processing. An uploaded file cannot do this — ChatGPT would treat it as a document to analyse rather than as a governing instruction. The copy-paste method ensures the instruction is received as a direct command.

Do not attempt to upload the opening instruction block as a file. Copy and paste it exactly as written in the RunSetup document.

\---

## Note on the Canon

The Canon is loaded multiple times during a full 3 module run — once into the Claude companion session during Phase 2 initialisation of `SRIT_Claude_SysDesc_v0_4_4`, and once into each fresh ChatGPT session at the start of each new module run. This is correct and necessary. Claude and ChatGPT are independent sessions — each requires the Canon as its governing context.

\---

## Session Overview

|#|Platform|Session|Opens|Closes|
|-|-|-|-|-|
|1|Claude Sonnet 4.6|Companion session|Before SRIT begins|After DDA Commentary Summary is saved|
|2|ChatGPT GPT-5.4|SRIT execution|Full Run Step 2|After SRIT Run Record pasted to Claude|
|3|ChatGPT GPT-5.4|DAI execution|Full Run Step 12|After DAI Run Record pasted to Claude|
|4|ChatGPT GPT-5.4|DDA execution|Full Run Step 21|After DDA Run Record pasted to Claude|

The Claude companion session is never closed between modules. The three ChatGPT sessions are each opened fresh and closed after the Run Record is handed to Claude.

\---

## Full Run Sequence

### Before the run

**1.** Open a new Claude Sonnet 4.6 session. Upload `SRIT_Claude_SysDesc_v0_4_4.md`.

Submit.

Claude will read the file and open Phase 1 — the system description interrogation. Answer Claude's questions. Claude will probe each answer for precision before moving to the next.

When all four questions are complete, Claude will produce the **System Definition Statement** as a labelled copyable block. Confirm it is correct. Claude will lock it and transition automatically into Phase 2.

In Phase 2, drag the following four files into the session when Claude requests them:

- `Scarcity_Denial_Canon.md`
- `SRIT_Prompts_v1_8.md`
- `DAI_Prompts_v1_7.md`
- `DDA_Prompts_v1_5.md`

Submit.

Claude will confirm receipt, state its companion role, and signal readiness. Do not close this session for the remainder of the run.

---

### SRIT module

**2.** Open a fresh ChatGPT session. Pin model to GPT-5.4 Thinking Extended manually — do not use auto mode.

**3.** Drag and drop into ChatGPT in this order:

- `Scarcity_Denial_Canon.md`
- `SRIT_Prompts_v1_8.md`

Submit.

**4.** Copy the opening instruction block from `SRIT_ChatGPT_RunSetup_v0.1.txt` and paste it into ChatGPT. ChatGPT will confirm it has read the documents and wait for the system description.

Submit.

**5.** Paste the System Definition Statement produced by Claude in Phase 1 and Submit. This will then automatically complete Prompt 1.

**6.** After each prompt output, use **Copy response** from ChatGPT and paste it to the Claude companion session. Read Claude's commentary. If Claude provides a carry-forward note, paste it to ChatGPT alongside `Proceed.` If there is no carry-forward note, type `Proceed.` alone.

Submit.

**7.** After Prompt 5 output has been reviewed by Claude, type `Proceed.` in ChatGPT to run Prompt 6 Stage 1. ChatGPT will produce the complete declaration output and stop before the Run Record.

**8.** Use **Copy response** from ChatGPT to copy the complete Prompt 6 Stage 1 output and paste it to the Claude companion session. Into this same Claude session upload `SRIT_Claude_Review_v0_3_4.md`.

Submit.

Claude will review the declaration against the Canon, assessing: resource/mechanism distinction, selection rationale grounding, strongest alternative rejection, confidence rating consistency, DAI entry test question quality, whether each candidate eliminated under R6 at Prompt 4 has a complete adversarial challenge record (challenge argument, counter-argument grounded in the Canon's second sentence, disposition statement — any R6 elimination missing its record, or with a counter-argument that does not demonstrate the mechanism/resource distinction, will be flagged as a concern blocking Stage 2), and whether the Protectable Resource Form (Prompt 6 Section B) is present and operationally specific — specifying what must be preserved, in what state, at what level, and what substitution would fail (absence or imprecision will be flagged as a concern; an adequate form will be confirmed as pre-populating the DAI Prompt 2 Required Denial Specification Table).

If Claude identifies concerns, resolve them in ChatGPT before proceeding. If Claude confirms the declaration is ready, return to ChatGPT and type `Execute Run Record.`

**9.** When ChatGPT produces the Run Record code block, use **Copy** from the top right of the code block and paste it to the Claude companion session. Claude will ask for your local time, format the Run Record, and produce both files:

- `SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

**10.** Save both files.

---

### SRIT → DAI boundary

**11.** Upload `DAI_Claude_BoundaryCheck_v0_3_3.md` to the Claude companion session. Claude will check the SRIT Run Record for completeness, confirm readiness, and state the Binding Scarce Resource Declaration for confirmation.

Submit.

When Claude confirms Ready, upload `DAI_Claude_Review_v0_3_4.md` to the same Claude session. Claude will confirm it is loaded and ready. Do not open the DAI ChatGPT session until Claude confirms the Review file is loaded.

Submit.

---

### DAI module

**12.** Open a fresh ChatGPT session. Pin model to GPT-5.4 Thinking Extended manually — do not use auto mode.

**13.** Drag and drop into ChatGPT in this order:

- `Scarcity_Denial_Canon.md`
- `DAI_Prompts_v1_7.md`
- The SRIT Run Record (`SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`)

Submit.

**14.** Copy the opening instruction block from `DAI_ChatGPT_RunSetup_v0.1.txt` and paste it into ChatGPT. Type `Proceed.` to begin Prompt 1.

Submit.

**15.** After each prompt output, use **Copy response** from ChatGPT and paste it to the Claude companion session. Read Claude's commentary. If Claude provides a carry-forward note, paste it to ChatGPT alongside `Proceed.` If there is no carry-forward note, type `Proceed.` alone.

Submit.

At the end of Prompt 2 the run stops for the Evidence Register:

- **Evidence available** — upload `DAI_Evidence_Register_v0_2.md` to the Claude companion session. Claude will render the Evidence Register tool. Complete the register, export, paste back to Claude for pre-screening, and when Claude confirms clearance paste to ChatGPT and type `Proceed.` for Prompt 3. Submit.
- **No evidence** — type `SKIP` in ChatGPT. ChatGPT will then present four reason codes. Select the code that best describes the reason for skipping:

  - **S1 — No relevant evidence available**
  - **S2 — Evidence exists but not yet gathered**
  - **S3 — Evidence exists but access is restricted**
  - **S4 — Desktop run only — evidence not sought**

  Confirm your selection. ChatGPT will record the code before proceeding to Prompt 3. Do not proceed without selecting a code — retrospective recording is not permitted.

After the Prompt 3 Actual Denial Mapping Summary is produced, ChatGPT will check the evidence distribution. If the mapping is predominantly inferred, ChatGPT will issue a Near-Threshold Evidence Notice or Critical Near-Threshold Evidence Notice and stop.

At that point:
- Type **CONTINUE** to accept the inferred mapping and proceed to Prompt 4.
- Type **PAUSE** to return to evidence admission before the mapping closes.

If you type PAUSE: return to the Evidence Register workflow, admit new evidence through the Validation Stage, then rerun Prompt 3 from scratch. Do not resume mid-output.

If no threshold notice appears, proceed normally.

**16.** After Prompt 4 output has been reviewed by Claude, type `Proceed.` in ChatGPT to run Prompt 5 Stage 1. ChatGPT will produce the complete Denial Architecture Judgement output and stop before the Run Record.

**17.** Use **Copy response** from ChatGPT to copy the complete Prompt 5 Stage 1 output and paste it to the Claude companion session. Claude will review the judgement against the Canon. If Claude identifies concerns, resolve them in ChatGPT before proceeding. If Claude confirms the judgement is ready, return to ChatGPT and type `Execute Run Record.`

**18.** When ChatGPT produces the Run Record code block, use **Copy** from the top right of the code block and paste it to the Claude companion session. Claude will ask for your local time, format the Run Record, and produce both files:

- `DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

**19.** Save both files.

---

### DAI → DDA boundary

**20.** Upload `DDA_Claude_BoundaryCheck_v0_4.md` to the Claude companion session. Claude will check the DAI Run Record, confirm the Readiness for Drift Analysis gate, state the Denial Architecture Status and its DDA starting posture.

Submit.

---

### DDA module

**21.** Open a fresh ChatGPT session. Pin model to GPT-5.4 Thinking Extended manually — do not use auto mode.

**22.** Drag and drop into ChatGPT in this order:

- `Scarcity_Denial_Canon.md`
- `DDA_Prompts_v1_5.md`
- The DAI Run Record (`DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`)

Submit.

**23.** Copy the opening instruction block from `DDA_ChatGPT_RunSetup_v0.1.txt` and paste it into ChatGPT. Type `Proceed.` to begin Prompt 1.

Submit.

Prompt 1 produces three outputs: the DDA Input Receipt Table (Section A), the Drift Boundary Lock Statement (Section B), and the Finding Stability Frame (Section C). The Finding Stability Frame records the principal unresolved dimension carried from DAI, the primary rival interpretation to test, and the opening trajectory posture. It does not constitute a drift judgement. It will be reviewed and confirmed or revised at Prompt 5 Stage 1 Section F.

**24.** After each prompt output, use **Copy response** from ChatGPT and paste it to the Claude companion session. Read Claude's commentary. If Claude provides a carry-forward note, paste it to ChatGPT alongside `Proceed.` If there is no carry-forward note, type `Proceed.` alone.

Submit.

**25.** After Prompt 4 output has been reviewed by Claude, type `Proceed.` in ChatGPT to run Prompt 5 Stage 1. ChatGPT will produce the complete Drift Detection Judgement output — Sections A through F — and stop before the Run Record.

The Prompt 5 Stage 1 section map is:

| Section | Content |
|---------|---------|
| A | Drift Detection Judgement |
| B | Drift Trajectory Assessment |
| C | Strongest Counter-Interpretation |
| D | Minimum Intervention Logic |
| E | Empirical Tests for Next Stage |
| F | Finding Stability Review |

**26.** Use **Copy response** from ChatGPT to copy the complete Prompt 5 Stage 1 output — Sections A through F — and paste it to the Claude companion session. Into this same Claude session upload `DDA_Claude_Review_v0_4.md`.

Submit.

Claude will review the judgement against the Canon. If Claude identifies concerns, resolve them in ChatGPT before proceeding. If Claude confirms the judgement is ready, return to ChatGPT and type `Execute Run Record.`

The DDA Run Record contains 16 sections. If the Run Record is too large for a single code block, ChatGPT will split it:
- First block: Run Metadata through Drift Signal Summary
- Second block: Boundary Displacement Test Table through Finding Stability Review

Use **Copy** from the top right of each code block. If two blocks are produced, paste them to the Claude companion session in order.

**27.** When ChatGPT produces the Run Record code block(s), paste to the Claude companion session. Claude will ask for your local time, format the Run Record, and produce both files:

- `DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

**28.** Save both files.

---

### End of run

**29.** The six artefacts are the complete auditable output of the pipeline:

- `SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

The Claude companion session may now be closed.

---

Claude produces all Run Record and Commentary Summary files. The naming convention is:

```
SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md
SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md
DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md
DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md
DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md
DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md
```

Time is local time at point of file creation. Claude will ask for local time before producing each file.

\---

## Module Boundary Decisions

### SRIT → DAI

**Proceed if:** Confidence rating is 6 or above and the Run Record contains all nine sections.

**Do not proceed if:** Confidence rating is 5 or below. Gather the Stage 1 Test Questions empirical evidence and rerun SRIT.

**Proceed with caution if:** A tightly coupled co-binding condition is present — confidence 7 or below, two candidates explicitly described as co-binding in the residual uncertainty section. Claude will flag this at the boundary check. Ensure it is carried into the DAI run.

### DAI → DDA

**Proceed if:** Readiness for Drift Analysis shows Ready.

**Do not proceed if:** Readiness for Drift Analysis shows Not Ready. Review the Primary Evidence Weakness from DAI Prompt 3 and determine whether a second DAI run with Evidence Register data would resolve it.

**Note** the Denial Architecture Status confirmed by Claude at the boundary check — it determines the DDA starting posture.

\---

## What to Do When a Module Produces an Unexpected Result

**Boundary Viability Halt in SRIT** — boundary drawn too narrowly. Close the ChatGPT session. Return to the Claude companion session and instruct Claude to reopen the system description from Phase 1 Question 2 to redefine the boundary. Claude will produce an updated System Definition Statement. Begin the SRIT run again.

**Scarcity re-opening triggered in DAI Prompt 1** — DAI has identified an inconsistency in the SRIT Run Record. Read the trigger reason. If genuine, return to the SRIT Run Record and correct it. If incorrect, instruct: *The scarcity is closed. Treat the declaration as fixed.*

**Not Ready at DAI Prompt 5** — do not proceed to DDA. Review DAI Prompt 3 evidence status and consider whether the Evidence Register would produce a more complete mapping.

**Indeterminate at DDA Prompt 5** — record the Run Record as provisional. The Empirical Tests for Next Stage identify what would resolve the indeterminacy.

**Claude review identifies a material concern** — do not instruct Stage 2 until resolved in ChatGPT. If the concern cannot be resolved within the session, note it in the Run Record as a known limitation.

\---

## Session Discipline

* The Claude companion session opens once and stays open for the full three-module run
* Every ChatGPT execution session starts fresh — new chat, model pinned manually to GPT-5.4 Thinking Extended
* Paste every ChatGPT prompt output to Claude before instructing the next prompt
* Upload the relevant Claude instruction file at each Stage 1 and boundary point — do not skip these steps
* Do not close a ChatGPT session between Stage 1 and Stage 2 of the final prompt
* The six artefacts produced by Claude are the complete auditable record of the run

\---

*Version 0.5.2 — companion to SDF_User_Manual_v0.2 · SRIT v1.8 · DAI v1.7 · DDA v1.5*

*© Philip Harry Galvin 2026. The Scarcity–Denial Canon, SRIT, DAI, and DDA instruments are licensed under Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0). Free use for non-commercial purposes with attribution. No derivative works. Commercial use or modification requires prior written approval from the author.*
