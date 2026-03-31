# SRIT Run Record

## Run Metadata
- **System:** West Africa regional electricity grid — regional coordination and dispatch layer
- **Run Date/Time:** 2026-03-31 12:51
- **AI Model:** GPT-5.4 Thinking
- **Thinking Mode:** enabled
- **SRIT Version:** 2.2
- **Scarcity Type (optional):**

---

## System Definition Statement

**System:** West Africa regional electricity grid — regional coordination and dispatch layer

**Boundary:** Includes the regional coordination body (WAPP), cross-border dispatch arrangements, interconnection operating agreements, member-state system operators in their regional coordination capacity, and any operating instruments, rule sets, or binding procedures governing callable-generation availability decisions at the regional layer. Excludes generation assets below the regional dispatch layer, transmission infrastructure, upstream fuel supply chains, downstream end-user consumption, national energy policy and regulatory bodies, and financing and procurement functions.

**Failure Condition:** The regional coordination and dispatch layer cannot enforce a binding callable-generation adequacy boundary before regional usable callable generation falls below the level required to sustain load — evidenced by the absence of a pre-breach regional stop point, open override routes between member-state discretion and the required regional gate, or no evidenced actor with binding authority to refuse or reverse availability-reducing decisions across the regional operating boundary.

**Time Horizon:** 18–36 months

---

## Boundary Audit Table

| Candidate | Boundary Status | Reason |
|-----------|----------------|--------|
| Regional usable callable generation | Adjacent system signal | This is the resource the regional layer is attempting to preserve; the boundary includes the regional decision and control layer governing it, not the generation stock itself, and generation assets below the regional dispatch layer are excluded. |
| Regional callable-generation reserve margin | Adjacent system signal | This is an adequacy buffer in the underlying callable-generation layer feeding the regional coordination system rather than a resource residing inside the regional coordination and dispatch layer itself. |
| Availability rights over nominated generation | In scope | These rights reside in the regional operating instruments and availability-governing procedures explicitly included in the boundary. |
| Binding refusal authority over availability-reducing decisions | In scope | This sits directly inside the included regional actor, rule, and binding-procedure layer named in the boundary and failure condition. |
| Member-state compliance with regional dispatch obligations | In scope | Member-state system operators in their regional coordination capacity are explicitly inside the boundary. |
| Override-resistant operating discipline | In scope | This operates within the regional gate, override paths, and operating procedures included in the boundary. |
| Regional rule-set enforceability | In scope | Regional operating rule sets and their practical enforceability sit directly inside the included regional operating layer. |
| Cross-border dispatch information integrity | In scope | Shared dispatch information is part of the cross-border dispatch arrangements explicitly included in the boundary. |
| Reserve visibility across member states | In scope | Visibility over reserve at the regional coordination layer resides within the included regional coordination and dispatch process. |
| Regional coordination bandwidth | In scope | This is process and decision capacity inside WAPP and the cross-border coordination layer explicitly included in the boundary. |
| Escalation time before adequacy breach | In scope | This is a temporal operating resource inside the regional decision sequence that must exist before the defined failure point. |
| Operator adequacy-assessment capability | In scope | This capability sits within the regional coordination actor-set and operating process included in the boundary. |
| Institutional continuity of the regional coordinator | In scope | Continuity of the regional coordinating body resides within the included WAPP/regional coordination layer. |
| Trust and credibility between regional and national operators | In scope | This relational operating condition sits within the included regional coordination relationships between regional and member-state actors. |
| Executable cross-border dispatch options | Adjacent system signal | This spans included regional procedures and excluded generation and transmission states; under the conservative boundary rule it is treated as an adjacent operational-delivery signal rather than a resource wholly inside the defined layer. |
| Usable interconnection transfer headroom | Adjacent system signal | This resides in the excluded transmission infrastructure layer, even though it conditions whether regional decisions can be converted into usable supply. |

---

## Mechanism Gate Table

| Candidate | Step 1 Result | Standalone Failure Pathway | Governed Resource (if applicable) | Gate Result |
|-----------|---------------|----------------------------|-----------------------------------|-------------|
| Availability rights over nominated generation | Triggered | If regional availability rights are insufficient, nominated generation can be withdrawn from regional call despite adequate information, time, and coordination, so the regional layer cannot hold a binding adequacy boundary. | | Resource candidate |
| Binding refusal authority over availability-reducing decisions | Triggered | If no actor has binding refusal authority, the regional layer directly fails its service of stopping or reversing adequacy-eroding decisions across the regional boundary. | | Resource candidate |
| Member-state compliance with regional dispatch obligations | Triggered | Even with rules, information, and escalation time intact, non-compliance at the member-state operating point defeats regional enforcement and leaves the boundary non-binding. | | Resource candidate |
| Override-resistant operating discipline | Triggered | If override routes remain open, adequacy-reducing decisions can bypass the regional gate even when other inputs are notionally adequate. | | Resource candidate |
| Regional rule-set enforceability | Triggered | If regional rules are not practically enforceable, the regional layer cannot turn its procedures into binding adequacy protection before breach. | | Resource candidate |
| Cross-border dispatch information integrity | Triggered | If unit status and adequacy information are materially wrong or late, the regional layer can fail directly by acting too late or on a false adequacy picture. | | Resource candidate |
| Reserve visibility across member states | Triggered | If true reserve visibility is absent, the regional layer can fail directly by misidentifying what callable adequacy exists and where the pre-breach stop point lies. | | Resource candidate |
| Regional coordination bandwidth | Triggered | If coordination bandwidth is insufficient, the regional layer can fail directly because the required cross-border synchronisation cannot be completed before the adequacy boundary is crossed. | | Resource candidate |
| Escalation time before adequacy breach | Triggered | If the available escalation window is too short, the regional layer can fail directly because the pre-breach regional stop cannot be executed in time. | | Resource candidate |
| Operator adequacy-assessment capability | Triggered | If adequacy-assessment capability is insufficient, the regional layer can fail directly by not identifying breach proximity soon enough to activate the stop point. | | Resource candidate |
| Institutional continuity of the regional coordinator | Triggered | Loss of continuity weakens the maintenance and carrying power of authority, rules, information, and capability, but does not by itself demonstrate a standalone service-production failure if those remain notionally adequate. | authority, rule-set enforceability, information integrity, coordination capability | Mechanism — eliminate |
| Trust and credibility between regional and national operators | Triggered | Its failure pathway runs mainly through weaker information-sharing, slower escalation, and poorer compliance rather than through direct standalone failure of regional boundary enforcement. | information integrity, escalation responsiveness, compliance | Mechanism — eliminate |

---

## Adversarial Challenge Record(s)

None.

---

## Candidate Mechanism-Layer Items for DAI

- Institutional continuity of the regional coordinator — governs authority, enforceability, information integrity, and coordination capability — its failure works mainly by weakening the carrying structure of other service-production resources rather than acting as the direct resource consumed in boundary enforcement.
- Trust and credibility between regional and national operators — governs compliance, information-sharing, and escalation responsiveness — its failure pathway runs mainly through degradation of other shortlisted resources rather than direct standalone service-production failure.

---

## Adjacent System Signals

- Regional usable callable generation — the object to be protected by the regional layer may be the binding scarcity in the adjacent supply-adequacy system; may warrant a separate SRIT run.
- Regional callable-generation reserve margin — the adequacy buffer may be binding in the adjacent callable-generation layer; may warrant a separate SRIT run.
- Executable cross-border dispatch options — may be binding in the adjacent operational-delivery layer spanning callable supply and transfer execution; may warrant a separate SRIT run.
- Usable interconnection transfer headroom — may be binding in the adjacent transmission/interconnection operating layer; may warrant a separate SRIT run.

---

## Provisional Shortlist

The strongest remaining scarce resources are:

1. Binding refusal authority over availability-reducing decisions
2. Regional rule-set enforceability
3. Cross-border dispatch information integrity
4. Regional coordination bandwidth
5. Escalation time before adequacy breach

Why these remain:
- Each sits inside the locked regional coordination and dispatch boundary rather than in the excluded generation or transmission layers.
- Each has a direct relationship to the regional layer's defined service: producing a binding pre-breach adequacy boundary.
- Each requires continual preservation and shows weak durable substitution once the system is under stress.

Outstanding ambiguity:
- The unresolved issue is whether the dominant scarcity is primarily institutional, informational, organisational, or temporal at the regional layer, and whether rule-set enforceability is analytically distinct from binding refusal authority or merely its formal operating expression.

---

## Prompt 5 Late-Catch Retest Log

- **Candidate:** Binding refusal authority over availability-reducing decisions
- **Late-catch check:** Applied — no mechanism character identified in weakening evidence
- **Result:** Remains on ranking
- **Ranking recomputed:** Not applicable

- **Candidate:** Regional rule-set enforceability
- **Late-catch trigger:** Weakening evidence indicates that enforceability may operate through whether authority and compliance can actually bite, raising possible mechanism character.
- **Step 2 retest result:** Resource candidate — remains on ranking
- **Ranking recomputed:** No

- **Candidate:** Cross-border dispatch information integrity
- **Late-catch check:** Applied — no mechanism character identified in weakening evidence
- **Result:** Remains on ranking
- **Ranking recomputed:** Not applicable

- **Candidate:** Regional coordination bandwidth
- **Late-catch trigger:** Weakening evidence raises possible mechanism character because failure may appear to run through mobilisation of authority, rules, and information rather than through direct depletion of bandwidth itself.
- **Step 2 retest result:** Resource candidate — remains on ranking
- **Ranking recomputed:** No

- **Candidate:** Escalation time before adequacy breach
- **Late-catch check:** Applied — no mechanism character identified in weakening evidence
- **Result:** Remains on ranking
- **Ranking recomputed:** Not applicable

---

## Binding Scarce Resource Declaration

In West Africa regional electricity grid — regional coordination and dispatch layer, at the regional authority and operating-boundary level, over an 18–36 months horizon, the binding scarce resource is binding refusal authority over availability-reducing decisions, because depletion, misallocation, or failed protection of this resource causes primary system instability and cannot be durably substituted.

---

## Protectable Resource Form

What must be preserved is a regionally operative power to refuse, halt, or reverse any availability-reducing decision that would push regional usable callable generation below the level required to sustain load.

The resource must exist in the following operational form:
- as a pre-breach stop point
- exercisable at the regional layer
- usable before member-state discretion, procedural delay, or override routes can erode adequacy
- attached to an identified actor, rule path, or decision instrument with practical binding effect across the regional operating boundary

Nominal presence is inadequate where:
- authority exists only on paper but cannot be operationally exercised in time
- reversal power depends on voluntary compliance, persuasion, or post-breach escalation
- override routes remain open between member-state discretion and the required regional gate
- authority cannot reach the actual decision point where callable availability is reduced

Apparent substitutes fail under the declared failure condition because:
- regional rule-set enforceability without actual refusal power can leave rules advisory or contestable
- coordination bandwidth can accelerate process but cannot bind a decision it has no power to stop
- information integrity can reveal the approach to breach but cannot itself refuse the decision
- escalation time can widen the window, but more time does not solve absence of a binding stop once the decisive actor remains unable to deny the reduction

---

## Selection Rationale

Why this resource was selected:
- It is the candidate with the closest and most explicit fit to the locked failure condition from Prompt 1, which directly names the absence of an actor with binding authority to refuse or reverse availability-reducing decisions as a defining failure marker.
- It sits fully inside the locked system boundary, which is not the generation layer itself but the regional coordination, dispatch, operating-instrument, and binding-procedure layer.
- It explains the primary failure more directly than the remaining candidates: the regional layer fails because it cannot produce a binding pre-breach adequacy boundary.
- It survives the Prompt 5 evidence review as the strongest candidate on structural fit and crisis relevance.
- The remaining candidates are all materially important, but each is weaker as a final declaration because each either supports, formalises, informs, accelerates, or conditions the exercise of the stop point rather than constituting the stop point itself.

---

## Strongest Alternative Rejected

Strongest alternative candidate: Regional rule-set enforceability

Why it was rejected:
- It is the strongest alternative because it also sits squarely inside the included regional operating layer and explains why procedures may fail to bite.
- It was rejected as the final declaration because, on the current record, it is more plausibly the formal operating expression of binding refusal authority than a deeper scarcity distinct from it.
- The failure condition is framed around whether the regional layer can actually refuse or reverse adequacy-reducing decisions, not merely whether it possesses procedures that look enforceable.
- A rule set can be formally coherent yet still fail at the decisive point if no actor can operationally wield binding refusal power across the regional boundary.
- If the present declaration is wrong, the most likely alternative scarcity is regional rule-set enforceability, with regional coordination bandwidth the next most plausible non-institutional challenger.

---

## Confidence and Residual Uncertainty

Confidence rating: 7/10

Residual uncertainty:
- The main unresolved issue is whether binding refusal authority and regional rule-set enforceability are analytically separable in this system or whether the latter is simply the executable form of the former.
- The declaration is operationally specific enough to support downstream analysis, but the exact actor-path-instrument combination carrying the protectable authority remains unverified on the current record.
- A further uncertainty is whether regional coordination bandwidth becomes dominant in practice once authority is assumed to exist, particularly under compressed pre-breach conditions.
- If the protectable resource form is only partly evidenced, DAI will need to test whether the stop point is truly absent, merely mislocated, or present in formal terms but non-binding in operation.

---

## DAI Entry Test Questions

- What specific regional actor, instrument, or procedure — if any — can refuse or reverse an availability-reducing decision before adequacy breach?
- Is that authority legally binding, operationally binding, or only advisory in practice?
- At what exact decision point does the regional stop need to bite, and does the identified actor actually reach that point?
- What override routes remain open between member-state discretion and the required regional gate?
- Where regional rules exist, do they compel action directly, or do they rely on separate authority that may be absent or contested?
- Has any regional procedure ever actually blocked, reversed, or prevented an adequacy-eroding decision across the regional operating boundary?
- If authority appears formally present, what evidence shows it can be exercised in time under stress?
- Does coordination failure explain observed breakdown better than authority absence once the decision point is examined directly?
