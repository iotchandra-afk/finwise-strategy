# The Solution | FinWise

### Visual: first value worth trusting

![The first value: a verified, defensible owner cash decision](../visual-story/06_The_First_Value.png)

[See the complete slide sequence](../visual-story/README.md).

> **Module 2: Acquisition & Activation**  
> **Product decision:** Build a *decision-first* onboarding path that gets an owner-operated small business to a defensible cash decision with minimal setup and explicit data-quality checks.  
> **Evidence status:** A prototype and a testable design hypothesis, **not** a measured conversion improvement or a demonstrated FinWise capability.

## 1. Aha moment: a decision the owner can defend

**Proposed Aha:** *“I can see when a late customer payment could put payroll or an essential bill at risk, understand what the forecast assumes, and decide what to do before the cash gap occurs.”*

The important word is **defend**. In small-business finance, a fast but untrustworthy answer is not activation. A business owner might act on it, discover that a payroll tax, an uncleared deposit, or a duplicate inter-account transfer was missing, and never trust the product again.

Our first learning segment is **owner-operated businesses with variable receivable timing and no dedicated finance team**. This is a proposed wedge, not a known customer profile from the case. Accountant-led and finance-team use cases should be evaluated separately; collapsing them into one funnel hides different jobs, authority, and decision cadences.

**The unit of value:** one *verified financial decision*, not one import, a pretty chart, a clicked recommendation, or a session over five minutes.

To qualify as an actual Aha event in a production FinWise trial, one eligible business must:

1. Bring its **own** permitted financial data into a usable state, with recency and material exceptions surfaced. Synthetic demonstration data never qualifies.
2. Select a relevant near-term question, review a scenario that incorporates dated obligations and uncertain receipts, and understand the material assumptions.
3. See an intelligible answer: projected low cash, *when* it happens, comparison to a user-set operating floor, and the event driving the difference.
4. Save or explicitly acknowledge one decision with its trigger for review and the source/assumption version, rather than simply viewing an output.

The user should be able to explain the decision in ordinary language, without requiring an analyst to translate the dashboard. The product can measure actions 1–4, but **understanding and trust need qualitative validation** through usability sessions and follow-up interviews.

### What Module 1 commits us to, and what it does not

Module 1 prioritized learning whether the path `real data → usable answer → business decision → second review` can improve durable adoption. The case only establishes **2% trial-to-paid conversion, 40% one-year paid retention, and overdependence on paid signups**. It does not prove that onboarding causes either commercial problem. Poor acquisition fit, infrequent need, and reverse-trial entitlements remain rival explanations. Module 2 creates a concrete intervention to investigate H1 without suppressing those alternatives.

## 2. Onboarding prototype

**[Open the interactive prototype](./onboarding-prototype.html)** (standalone HTML in this folder; download/open locally, or serve it as a static page). It requires no framework, login, backend, banking permission, or external assets.

The prototype uses a clearly labeled **fictional** 14-day ledger. It has no live FinWise integration, real financial advice, actual reminders, or payment execution. Its purpose is to let peers test the proposed sequence and judgment boundaries, not to create false evidence of activation.

| Moment in the experience | Prototype behavior | Why it earns its place |
| --- | --- | --- |
| **1. Ask the job** | “Will I have enough for payroll and bills?” instead of a feature tour. Alternative purchase-planning job is visibly out of scope. | Reduces abstract setup; anchors the model to a consequential, recurring question. |
| **2. Inspect data and exceptions** | Shows starting cash, expected inflows, scheduled outflows and two receivables with uncertain collection dates. User acknowledges the limitations before continuing. | Confidence must come from visible inputs and caveats, not a manufactured “accuracy score.” |
| **3. Stress-test timing** | Toggle late payment by customer and change the cash floor. Compare the on-time and stressed balance day by day. | Makes the *causal lever* legible. Seeing a projected cash dip is more useful than receiving a generic low-cash warning. |
| **4. Record a decision** | Capture next action, earliest review trigger, and the scenario assumptions; simulate a changed payment status and review again. | Converts a view into accountable work and hints at a repeat job. No automatic external action. |

**Illustrative prototype outcome, not a real customer result:** Opening cash is $42,500; two invoices totaling $19,500 may arrive late; payroll and other dated obligations still occur. At a $20,000 buffer, the on-time low is **$29,100 on day 11**. If both invoices are late, cash first drops below the floor on **day 7**, bottoms at **$9,600 on day 11**, and requires **$10,400** of additional buffer or equivalent changes to planned cash flows to maintain that floor. This calculation uses end-of-day balances; intraday liquidity and unlisted obligations are excluded. The prototype exposes the arithmetic for scrutiny.

**A strong candidate Aha statement after that interaction:** “If both customers pay late, I cross my minimum cash threshold on payroll day. I need to confirm collections or arrange approved liquidity before day 7, and I know which assumptions to recheck.”

The user, not FinWise, owns that choice. Suggested actions are reviewable options, not unapproved transfers or autonomous borrowing instructions.

### What a production implementation would require

The prototype demonstrates intended UX, **not existing FinWise feature inventory**. Before building, validate available imports, product entitlements, trial length, and data model. Minimum production requirements:

- **Cash semantics:** Separate bank-cleared cash from invoiced revenue; do not treat accounts receivable as deposited money. Account for duplicate transfers, pending items, payroll taxes, and obligations not present in a bank feed.
- **Source trust:** Display as-of times, missing data, reconciliation flags, and input corrections. Route material gaps to *“cannot answer reliably yet”*, not a numerically precise guess.
- **Access and consent:** Use permissioned, read-only financial access where possible, minimal data retention, role-based sharing, and no credentials entered into a simulated connector. Never auto-share financial scenarios with an accountant.
- **Traceability:** Save the question, data snapshot/version, assumptions, user edits, decision, and review trigger. If data later changes, show **what changed**; do not silently rewrite the original recommendation.
- **Reverse-trial boundary:** Confirm which capabilities remain when premium access expires. An Aha that disappears before the pay decision may be a packaging failure rather than an onboarding failure, a question for Module 6.

## 3. Communication and personalization plan

The onboarding prompt supplied with the course asks for stages, segments, message type, frequency, limitations, purpose, and copy. The core rule is **respond to demonstrated friction**, not bombard every new trial with the same sequence. Messages below are *proposed*, not sent or configured.

| Stage | User segment / signal | Message type and frequency | Prompt message | Purpose and limitation |
| --- | --- | --- | --- | --- |
| **Entry** | Owner-operated, cash-timing job selected | In-product, once at entry | **“Which decision do you need to make this week?”** Choose payroll and bills, or another job. | Establish intent before requesting financial access; do not infer a job from ad targeting alone. |
| **Connection paused** | Chose job but has not imported usable data | Contextual in-product next visit; at most one opt-in email in 48 hours | **“We can show the impact of late payments once your balances and due dates are ready. Want to review what’s missing?”** | Diagnose permission, format, or anxiety. Do not call demo data “activated” or repeatedly ask for credentials. |
| **Quality exception** | Import succeeded but key obligation or receipt is stale/unmatched | In-product at the point of use; no promotional email | **“Two expected payments are not confirmed. Review their timing before relying on this forecast.”** | Stop false confidence. If inputs remain materially incomplete, block a “verified decision” event and offer correction/support. |
| **Answer ready** | Valid scenario, no saved decision | One contextual prompt after answer | **“Your lowest projected cash is on day 11. Which change will you check before your next payroll?”** | Move from chart to customer-owned action. Never imply the model guarantees solvency. |
| **Decision recorded** | Saved action and review trigger | Confirmation immediately; later only at chosen trigger and with appropriate consent | **“You saved the assumptions behind this plan. Revisit it when a payment clears or an obligation changes.”** | Make return use purposeful. A generic “log in daily” streak would measure habit pressure, not financial utility. |
| **No return / exit** | No second meaningful review by day 28 | At most one consented value-oriented follow-up; suppress after opt-out | **“Has the cash question changed? If so, the next review should take less work. If not, there’s nothing you need to do.”** | Respect episodic need. This behavior may disprove the recurring-job hypothesis rather than justify more nudges. |

For an accountant persona, do not simply swap the salutation; the job may be multi-client exception triage with explicit client authorization. That should be a separate discovery track, not a personalization flag in the first owner flow.

## 4. Why this should activate, and when it will not

**Causal mechanism proposed:**

`specific decision intent → sufficiently trustworthy data → explainable scenario → self-owned action → lower effort to review new facts`

This design attacks *time to meaningful value*, not time to first click. It minimizes setup that does not change the answer, but accepts necessary friction for financial correctness. Trust is part of the product, not a compliance step to decorate later.

| Design choice | Trade-off an experienced PM should recognize | What would change our mind |
| --- | --- | --- |
| Ask for the decision before integrations | Stronger relevance, but users may not yet know what question FinWise can answer. | If users cannot choose a credible job, test worked examples **without** counting them as activation. |
| Show uncertain invoices explicitly | More cognitive load, but concealing uncertainty creates false precision. | If users misread scenarios despite explanation, redesign assumptions and model labeling before scaling. |
| Optimize for a saved decision | More meaningful than dashboard views, but can incentivize low-quality “save” clicks. | Audit a sample for genuine decisions and review usefulness, not just event counts. |
| Trigger return on changed facts | Fits business cadence, but may yield fewer sessions than daily reminders. | If the natural job is too episodic to support paid retention, revisit target segment or packaging rather than manufacture activity. |

### Known failure paths and the product's response

1. **Connection fails or permissions are denied:** Explain what data is needed and why; allow a safe retry or a separately labeled learning-only example. Do not mark activation.
2. **Model cannot reconcile essential balances or obligations:** Surface the unresolved exception, hold the verified-answer claim, offer human review or correction, and log diagnostic failure. Do not silently fill gaps with plausible numbers.
3. **User gets a valid answer but does not pay:** Investigate free-tier substitution, paywall timing, segment economics, and willingness to pay. More onboarding tips are unlikely to fix a mispriced product.
4. **User pays but never returns:** Test whether the business has a repeatable cash-planning job. A perfect first-use funnel can still produce poor 12-month retention.

## 5. Measurement and falsification plan

**Primary behavioral outcome (candidate 7-day verified activation):**

> `# eligible new trial businesses that complete a trustworthy, real-data scenario and save a decision within 7 days ÷ # eligible new trial businesses started in the same cohort`

Define eligibility **before treatment**, using stable business/account attributes. Do not denominator-switch to “businesses who connected data,” because doing so masks the largest onboarding obstacle. Count each business once, not every invited user. Synthetic walkthroughs and incomplete or untrusted imports stay outside the numerator.

| Measure | Exact purpose and cut |
| --- | --- |
| **Step funnel** | Trial start → decision intent → permissioned import → data quality pass → scenario understood/run → valid decision saved, with drop-off and elapsed time at every transition. |
| **7-day verified activation** | Primary early outcome by randomized assignment, original acquisition channel, business size, software source, and predeclared segment. |
| **28-day second meaningful review** | Repeat scenario with new facts, reconciled changes or user-revised assumptions, not an open/notification click. Track among **all** eligible trial starts and as a descriptive activated cohort measure. |
| **Commercial lagging outcomes** | Trial-to-paid conversion at the same point in the reverse-trial lifecycle, 90-day paying retention and mature 12-month paying-logo retention. Cohorts must be mature before interpreted. |
| **Trust/operating guardrails** | False or misleading cash answers, unresolved critical exceptions, connection failure, permissions/consent complaints, support minutes per eligible trial, and trial downgrade failures. |

**Instrumentation:** `trial_started`, `decision_intent_selected`, `import_attempted`, `import_usable`, `critical_exception_opened/resolved`, `scenario_completed`, `assumptions_acknowledged`, `decision_saved`, `decision_reviewed_after_change`, `trial_entitlement_changed`, `paid_started`, `paid_canceled`. Every event needs business ID, session/user role, timestamp, cohort/variant, data freshness, and an error taxonomy where applicable. Do **not** send invoice amounts, bank details or other sensitive raw financial information as general analytics event properties.

**Sequence of learning, with no fabricated lift:**

1. **Diagnose:** Review existing funnel, data availability, interview owners who activated and those who dropped, and inspect paywall timing and channel mix. If loss is predominantly *after* verified value, do not blindly build H1.
2. **Prototype-test:** Five to eight directional sessions across different owner contexts can expose comprehension and trust failures; they cannot estimate population conversion effects. Observe whether users can identify the first floor breach, driving assumptions, and a defensible action without coaching.
3. **Experiment if feasible:** Randomize *eligible businesses*, not sessions, to current onboarding vs decision-first onboarding. Pre-register 7-day verified activation as the early primary outcome, guardrails and analysis cuts. Respect sample size, seasonality, trial duration, and 2% paid conversion base rate. Follow paid conversion and retained value as lagging checks. Avoid declaring success on a proxy alone.

**Advance only if** comprehension, usable-data coverage and 7-day verified activation improve without materially degrading accuracy, consent, support burden, or paid outcomes. **Stop or redesign** when users misinterpret the model, errors rise, or verified value does not relate to repeat use. **Redirect the investment** if the dominant bottleneck turns out to be acquisition quality, episodic demand, or reverse-trial entitlements.

## 6. The lesson worth sharing with the cohort

> **The riskiest moment in financial SaaS is often when the product looks convincing before it is correct.** The best activation flow does not remove every step; it removes the steps that do not help a customer make a sound decision, while preserving the ones that make the answer defensible.

Module 2 makes a specific experience tangible. Module 3 should build the *changed-facts return mechanic*, Module 4 should use actual available signals to verify where users fail, and Module 5 should test the mechanism, rather than retroactively treating this design as proof.
