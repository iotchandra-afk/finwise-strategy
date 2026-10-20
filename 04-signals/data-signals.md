# The Signals | FinWise

> **Module 4: Data & Analytics**  
> **Finding:** FinWise has a two-stage commercial leakage pattern. It does **not** yet have evidence identifying the behavioral cause.  
> **Decision:** Measure the path to a trustworthy first decision and a verified second review, then establish whether those behaviors precede paid conversion and durable retention.  
> **Evidence status:** Case-supplied aggregate outcomes, transparent arithmetic, and a proposed analytics design. **No customer-level dataset, statistical correlation, observed feature-usage lift or causal effect is claimed.**

## 1. The data pattern we can actually defend

The supplied case establishes **2% trial-to-paid conversion**, **40% one-year retention among paying customers**, and a growth approach still dependent on acquiring trials through advertising. That is a multiplicative business-model problem, not evidence that people need more reminders or more product features.

| Funnel signal requested by the Module 4 worksheet | What the source actually provides | Defensible reading |
| --- | --- | --- |
| **Trial-to-paid conversion** | **2%**, aggregate case baseline | 98 in 100 trial starts do not become paying customers. We do not know where they disengage, who was qualified, or the reverse-trial entitlement boundary. |
| **One-year paid retention** | **40%**, aggregate case baseline | Six in ten paying customers are no longer retained at one year. The timing and reasons for churn are unknown. |
| **Durable paid yield from a trial cohort** | **0.8%**, *derived conditional illustration*: `2% × 40%` | Equivalent to **8 retained payers per 1,000 trials** only **if** both rates describe compatible start cohorts and follow-up windows. It is not a separately observed metric. |
| **Modeling usage and depth** | Not supplied | No legitimate claim about how modeling affects payment or repeat value. |
| **Import usage, successful reconciliation, coverage** | Not supplied | Cannot know if connectors, data quality or permissions are the activation bottleneck. An attempted import is not a usable financial state. |
| **Session duration and sessions/user** | Not supplied | Even if present, more time may signal confusion or anxiety rather than value. |
| **Illustrative engagement scorecard** | A sample weighted score of **6.7/10** | It is teaching material, not an observed FinWise score. Its DAU/MAU, duration and adoption weights should not drive this product. |

**The arithmetic makes prioritization unavoidable:** For an *illustrative* 1,000-trial cohort, 20 convert, 12 of those churn within a year and eight remain. Feeding more paid traffic into the same rates scales the leakage. It tells us **where commercial value is lost**, not **why**. In particular, the supplied material does not establish a correlation between imports, financial modeling, sessions and conversion.

**Product-leader interpretation:** The critical unknown is whether the early path to a **defensible financial decision** is broken, the **return-worthy job** is missing, the **customers acquired** are wrong, or the **reverse-trial packaging** interrupts value. These are competing explanations, not four proven causes. Modules 1–3 make the first two testable without prematurely declaring them true.

### What would change the diagnosis

| Observable signature, once real data exist | Likely competing explanation | Investment response |
| --- | --- | --- |
| Qualified owners fail between permissioned import, verified data and first saved decision; a randomized decision-first flow improves trustworthy completion. | **H1: Pre-value friction** | Fund the highest-loss, fixable activation step. Retain quality gates even when they add necessary friction. |
| Verified decisions and repeat use occur, but accounts stop paying when reverse-trial capabilities change. | **H3: Entitlement or willingness-to-pay mismatch** | Test feature boundaries and packaging, not more onboarding prompts. |
| Paid users complete valid decisions but encounter few consequential changes and rarely need another review. | **H4: The job is too episodic** | Change segment, job-to-be-done or monetization cadence. A low login rate alone is not evidence of failure. |
| Paid-acquired trials have weaker quality, activation and paid outcomes than comparable owner/business profiles from organic or referred sources. | **H2: Acquisition fit** | Reallocate distribution and tighten qualification before scaling demand generation. |
| The fastest-activating accounts experience false cash assurances, missing payroll obligations or high reconciliation support load. | **Financial trust failure** | Pause unsafe assurance paths; repair evidence integrity before optimizing any funnel metric. |

## 2. The correlation test: is product use a signal of value or merely intent?

**Testable association:** Among owner-operated SMB trials, are accounts making a **verified first decision** within seven days more likely to pay at the comparable trial transition and subsequently remain paid than accounts without one? Does a **second reviewed decision** predict later paid survival after accounting for each business's opportunity to receive a meaningful changed event?

**Unit of analysis:** One business account, not sessions, logins, users or device IDs. Freeze the trial-start cohort and eligibility **before** observing activation. Include failed imports and unsupported data journeys in the denominator; report their reasons separately. Preserve a stable business ID through reverse-trial downgrade, payment, cancellation and reactivation.

**Read sequence, not a misleading correlation:**

1. **Build one account-level timeline:** trial start, intent, source permission, first *reconciled and usable* data state, critical-obligation coverage, scenario review, valid decision saved, material event, second dispositioned review, entitlement change, payment and cancellation. Record timestamps and source versions.
2. **Compare like with like:** Hold or stratify on **pre-existing** owner vs accountant role, business size, cash-volatility proxy, acquisition channel, integration availability, trial offer and calendar cohort. Report absolute differences, confidence intervals and group sizes. Check missingness, bot/demo use, quality exceptions and support burden. Feature users are self-selected; a raw conversion gap is not evidence that a feature caused payment.
3. **Respect temporal ordering:** Seven-day activation can only be used as a predictor of conversion **after** that seven-day landmark; if the trial/pay transition occurs earlier, redefine the window before analysis. A day-28 review cannot be used to “explain” a day-14 payment decision. For retention, landmark paid accounts at the same elapsed tenure, handle right-censoring and compare future survival, not users who simply lived long enough to generate more events.
4. **Separate opportunity from response:** Track accounts with no material financial event or not-yet-available funds apart from those who ignored a valid prompt. A pending invoice marked paid cannot count as newly usable cash. Review at an explicitly chosen cadence can still be meaningful without an unsolicited alert.
5. **Look for a mechanism, then randomize:** A statistically clear association may reflect financial urgency, higher intent or connector compatibility. Module 5 should randomize the decision-first experience at the **business-account** level if the diagnosed friction is sufficiently common and the guardrails are viable.

**Correlation analysis to produce once event data are available:**

| Comparison | Numerator / denominator | Interpretation boundary |
| --- | --- | --- |
| Activation-to-conversion association | Paid accounts by the standardized conversion window / all eligible trial accounts, separately for those *with* and *without* verified day-7 activation | Descriptive, only when activation precedes the conversion outcome; adjust for cohort and pre-treatment mix. |
| Repeat-use-to-survival association | Accounts still paying at a future tenure milestone / all eligible paid accounts alive at a common landmark, split by verified second decision review | Avoid immortal-time and survivorship bias; event-opportunity strata reported. |
| Source/segment fit | Verified activation, payment and 90-day retention per eligible trial-start cohort by acquisition source and predefined business segment | Small cohorts, attribution gaps and channel-selection effects may limit inference. |
| Packaging break | Payment/handoff failures at entitlement transition among accounts that *already* achieved valid first value | If trust and use are healthy but payment collapses here, redirect toward Module 6. |

**No invented statistical result:** A correlation coefficient, p-value, lift, regression and “pattern in modeling usage” are **not computable** from the supplied Markdown templates or aggregate case rates. The finding above is a verified *aggregate commercial pattern*. The behavioral relationship is the next evidence request.

## 3. Leading indicators: behavior worth improving before the money arrives

| Indicator | Operational definition and timing | Why this is leading | Failure check |
| --- | --- | --- | --- |
| **L1. Seven-day verified activation** | `Eligible new trial businesses saving a defensible first real-data financial decision within seven days / all businesses eligible at trial start in that cohort`. Requires source freshness, usable funds semantics, relevant obligations, scenario/assumptions inspected and owner-recorded disposition. | Earliest substantive proof of the Module 1–2 Aha. Primary **near-term learning signal** for a decision-first onboarding intervention. | Do not count demo data, mere imports, partial reconciliation, abandoned decisions or businesses excluded *after* treatment. Read the rate alongside reason-coded failures and time-to-value p50/p90. |
| **L2. Twenty-eight-day verified second review** | `Activated businesses completing a subsequent evidence-backed decision review by day 28 / all activated businesses in that cohort`. A review may use verified changed facts or a customer-chosen substantive reassessment. Also report the **unconditional** share of *all* eligible trial starts reaching a second review. | Tests whether FinWise solves a recurring job rather than delivering a one-time impressive forecast; flows directly from Module 3's Decision Delta. | Exclude alert clicks, duplicated source versions and “paid in accounting but unavailable cash” status checks. Segment no-event accounts separately and show how many were actually eligible to receive a trigger. |
| **L3. Decision-readiness coverage** | `Businesses with fresh, reconciled available-cash evidence and explicit coverage of critical dated obligations / businesses attempting a financial decision`, with missing-data reasons. | The constraint that makes L1 and L2 credible; exposes whether more onboarding throughput would create dangerous confidence. | **Guardrail, not a volume target.** A payroll-tax gap, held funds, unknown cutoff or high-severity error blocks confident “all clear” even when the chart renders. |

**A metric system, not a single vanity index:** Report the three leading signals individually with denominators, cohort counts, distributions and failure codes. Do **not** roll them into a weighted score now. A team could raise L1 by loosening verification; L3 is there to detect and stop that behavior. Notification count, DAU and average minutes in session remain **diagnostics**, never the goal.

## 4. Lagging indicators: where the business case must ultimately prove itself

| Indicator | Definition / maturity | What would count as progress |
| --- | --- | --- |
| **G1. Trial-to-paid conversion** | `Businesses making first valid payment by the same documented trial/entitlement deadline / all eligible trial starts`, with cancel/refund policy consistent across cohorts. **Case baseline: 2%.** | A mature trial-start cohort improves without inferior customer fit, discount dependency, verification failures or worse retention. The actual reverse-trial length and payment window must be established before comparing. |
| **G2. Paid logo retention, 90 days and 12 months** | `Paying businesses surviving to each tenure mark / first-time paying businesses whose cohorts have matured to that mark`; distinguish voluntary cancel, involuntary failed payment, pauses and reactivation. **Case 12-month baseline: 40%.** | Repeat value carries into *sustained paid use*, not simply a longer trial. Show survival across time, not an annual percentage computed from immature accounts. |
| **G3. Durable cohort yield** | `Businesses still paying 12 months after first payment / eligible original trial starts from the corresponding conversion cohort`, with aligned windows. The **0.8%** figure is currently only the conditional `2% × 40%` illustration. | A product-led growth loop should create **more retained paying businesses per qualified trial** before marketing pays for another trial. |
| **G4. Economic quality and distribution** | Contribution per retained paying account after connector/data, reconciliation and support costs; plus qualified organic/referral trials and their paid yield. Requires revenue and cost data **not supplied**. | The business can serve and retain the account profitably, and customer-earned distribution reduces reliance on paid acquisition. A high review rate with negative account contribution is not success. |

**Read commercial metrics at account level and by cohort.** A product's bank-data accuracy, support burden, privacy complaints, false all-clears, missed material cutoff events and opt-out rate are **non-negotiable guardrails**. A severe false assurance is an incident to stop, not a trade-off to offset with higher conversion.

## 5. Minimum data contract to get from a thesis to a decision

| Data object / event | Minimum safe information to preserve | Why the field matters |
| --- | --- | --- |
| **Trial and account** | Pseudonymous `business_id`, pre-treatment eligibility, owner/accountant role, acquisition source, trial start, offer, entitlement and assigned test arm | Stable denominators; source and selection effects; no cross-account leakage. |
| **Data readiness** | Permission state, connector type, attempted/usable timestamps, data-freshness bucket, reconciliation state, *funds-available* state, missing-obligation exception class | “Imported” is not “safe to decide.” Never ship raw bank credentials or transaction memo text into general analytics. |
| **Decision record** | Decision ID, business ID, source/assumption version, chosen floor, *classification* of reviewed risk, owner disposition, revision reason and timestamp | Distinguishes real first/second value from a dashboard view or synthetic walkthrough. Store sensitive dollar-level detail only in authorized product systems. |
| **Review opportunity** | Verified event ID, materiality/cutoff classification, eligible role/channel, surfaced/suppressed decision, actual disposition and elapsed time | A non-return on a quiet account should not be conflated with ignoring an actionable event. Supports false- and missed-alert auditing. |
| **Business outcome** | Trial-entitlement transition, first payment, renewal, cancel/refund, 90-day and 365-day status, revenue/cost class | Closes the measurement chain through paid survival and account economics. |

**Data governance:** Consent and access by account/role; pseudonymize analytics IDs; keep raw financial amounts, account numbers, client names and payroll details out of broad event pipelines. Version the source and derived cash state; de-duplicate events and transfers; define event-time versus ingestion-time; audit late corrections and backfills. A CFO-grade data definition must survive a customer asking, *“Why did you say I could make payroll?”*

**Readout cadence:** Weekly new-trial funnel and exceptions, 28-day repeated-decision cohorts once mature, paid conversion aligned to each offer's entitlement transition, and quarterly rolling 90-day/12-month maturity reports. Segment initially by owner-operated cash-timing use case, channel and connection feasibility; publish uncertainty rather than overfitting tiny cells.

## 6. Decision gate for Module 5

Before declaring an experiment, request an account-level funnel extract plus an audited sample of rejected and accepted “verified decision” events. In parallel, interview owners who (a) never reached a trusted answer, (b) reached one but did not pay, and (c) paid and left. This distinguishes a product obstacle from a customer/job or packaging mismatch.

**Provisional next test if H1 survives diagnosis:** Compare existing onboarding with Module 2's **decision-first** flow. Randomize eligible business accounts; primary early outcome **L1 seven-day verified activation**; key downstream checks **L2, G1 and paid survival**; stop criteria include misleading cash verdicts, unreconciled obligations, permission incidents and untenable support effort. If the actual data point instead to the reverse-trial boundary or wrong acquisition mix, **do not** run the onboarding experiment merely because the prototype already exists.

At 2% paid conversion, modest relative conversion lifts are expensive to detect statistically. Module 1's illustrative 2.0%-to-2.4% comparison required roughly **21,100 trials per arm** under conventional 5% significance / 80% power assumptions. Module 5 must verify real traffic, exact trial length, minimum detectable effect, interference and read date. **A fast improvement in L1 is a useful learning signal, not proof of sustained revenue growth.**

> **The analytical lesson:** The most damaging product metric is one that can go up while the customer's decision gets worse. For FinWise, real value requires a trusted decision, an occasion to revisit it, and a business willing to keep paying for that help. Measure all three, in that order.

---

**Source boundary:** FinWise scenario and aggregate baselines from the supplied *Product Analytics & Experimentation Final Project Brief* (Product School, October 2026); the supplied `data-signals.md` worksheet and example engagement scorecard; and the hypotheses/prototypes in Modules 1–3. The course template repository contains **no trial-level dataset** in its Module 4 folder. All 14-day cash examples in Modules 2–3 are labeled **synthetic** and are not evidence of customer behavior.
