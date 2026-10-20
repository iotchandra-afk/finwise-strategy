# The Mechanic | FinWise

> **Module 3: Retention & Engagement**  
> **Mechanic:** *Decision Delta*, a trusted changed-facts review of a financial decision the customer already owns.  
> **Strategic choice:** Earn a return when the underlying decision may change. Do not design for a daily login streak.  
> **Evidence status:** Concept and interactive wireframe, not measured FinWise behavior or a verified product capability.

## 1. The mechanic

**The loop:** `save a decision → a material financial fact changes → see exactly what changed → reassess the decision → retain useful context for the next change`.

| Hook component | FinWise implementation hypothesis | What the customer actually experiences |
| --- | --- | --- |
| **Trigger** | A permissioned, reconciled event changes the risk or actionable outcome of a **saved** decision: a receivable clears or becomes materially overdue, an obligation changes, or a chosen review milestone arrives. | A privacy-safe cue: *“Your saved cash plan changed. Review it privately in FinWise.”* Never reveal payroll or account details in a push notification. |
| **Action** | Compare the saved scenario to the revised one, inspect changed assumptions and source freshness, and record **keep, revise, escalate, or no action** with a reason. | One review of the decision they previously made, not another full import or a generic dashboard visit. |
| **Reward** | Reduced uncertainty, earlier risk visibility, and less rework. Sometimes the answer is *“the original buffer plan is no longer necessary under these assumptions”*. | A defensible changed decision, or confidence that no change is warranted. This is a utility reward, not gamification. |
| **Investment** | Customer-controlled cash floor, original decision, exceptions, source/assumption version, review trigger and decision history. | The next review requires less reconstruction. Customers can correct, export, or delete their own context; the aim is usefulness, not lock-in. |

**Who it is for:** The Module 1–2 working segment, an owner-operated small business with irregular cash receipts and no dedicated finance team. A bookkeeper supervising many businesses has a different trigger/authority model and should not silently inherit this workflow.

**One return-worthy moment:** The Module 2 illustrative decision assumed that Customer A's $12,800 and Customer B's $6,700 invoices arrive late. With a $20,000 operating floor, its low point was **$9,600**, a **$10,400 gap**. Now Customer A's payment is **simulated as posted on day 5**. The revised low is **$22,400 on day 11**, giving **$2,400 headroom**. The modeled improvement is $12,800, exactly the changed receipt. The owner should reassess the planned buffer, while verifying Customer B, payroll taxes and unlisted commitments. No money is moved and no financial action is autonomously canceled.

This is a much more useful reason to return than *“You haven't logged in for seven days.”* Equally important, **when nothing material changes, the correct product behavior may be silence**.

## 2. Trigger contract: prevent an alert engine from eroding trust

FinWise is handling information that can influence payroll, supplier relationships and credit decisions. An inaccurate “all clear” is more dangerous than a missed engagement opportunity. Before emitting a decision-level alert, require all of the following:

1. **A decision exists:** It belongs to an authorized account and has a recorded cash floor, scenario assumptions, review status and a source version.
2. **A real change exists:** New source-event ID or user-confirmed obligation change; transaction freshness and posting/reconciliation state are visible. A mere forecast recalculation or unverified due date is not new evidence.
3. **It changes the decision materially:** For a *candidate* initial threshold, notify when the projected low changes by at least `max($1,000, 5% of the chosen cash floor)`, **or** crosses the chosen floor, **or** a critical payment/obligation changes status. These values need calibration; they are not learned from the supplied files.
4. **It is explainable:** Show old versus new facts, which item moved, its date, model version, and residual uncertainty. If key inputs are stale, present *“recheck your data before deciding”* rather than a confident balance claim.
5. **It is authorized and proportionate:** Honor channel consent and user role, bundle duplicate events, provide snooze/off controls, avoid financial details in email/push previews, and never autonomously approve borrowing, defer payroll, contact a customer or modify payment instructions.

**Operational limit:** One alert per material decision/version change, with idempotent event handling and sensible bundling; interrupt again only for a new genuinely consequential event. An exception resolution may itself be a useful trigger. Alert frequency should be measured as a *cost* borne by customers, not a growth target.

### Failure states that should stop the loop

| State | Safe response |
| --- | --- |
| Bank snapshot stale, import failed, transfer double-counted, or material obligation missing | Hold a confident cash verdict; explain the gap and offer correction/support. |
| Event comes from an account or role without permission | Do not use or expose it for this customer's decision. Log access-control failure internally. |
| Small change does not cross an action threshold | Keep history updated; no unsolicited prompt. |
| Customer already reviewed this source version | Suppress duplicate notification. |
| Trial's premium entitlement expired | Preserve access to decision history where the product permits, make entitlements explicit, and test whether loss of repeat utility is a packaging problem rather than an engagement problem. |
| Repeated apparent warnings prove incorrect | Pause the alert class, investigate false positives and reconcile errors before resuming. |

## 3. Wireframe: before, after, and a customer-owned next step

**[View the Decision Delta interactive wireframe](./decision-delta-wireframe.html)**. The standalone HTML can be downloaded and opened in a browser. It includes no real financial connections, external assets or messages sent.

| Visible area | Question it must answer |
| --- | --- |
| **Changed fact** | *What new evidence justifies interrupting me?* |
| **Prior versus revised low cash** | *How much did the answer change, and when?* |
| **Buffer crossing and 14-day curve** | *Is the original decision still relevant or did the risk merely move?* |
| **Assumptions and source audit** | *Why should I believe the new calculation? What remains uncertain?* |
| **Review/disposition and notification control** | *What am I going to do, what will I revisit, and when may FinWise contact me again?* |

The wireframe has four selectable synthetic states: A posted, B posted, both posted, and **no new evidence**. It recomputes the same day-level cash model as Module 2, lets the user record a reviewed decision, and previews how channel and materiality preferences affect a hypothetical alert. A click or open by itself does **not** record meaningful engagement.

## 4. Why it can retain, and why it might fail

**Product hypothesis:** Once a customer has made a trusted first decision, later reviews become valuable *if* FinWise remembers the original question and reduces the effort to interpret changed facts. This creates repeat value before the payment decision and may create a reason to retain the subscription after the novelty of the first forecast fades.

The behavior is **event-driven or cadence-driven**, not necessarily daily. Many good SMB owners have a weekly cash rhythm, except when a significant payment or obligation changes. A daily active-user spike could mean a worried owner is repeatedly checking an unresolved cash problem. A 40-second resolved review may be worth more than a 20-minute session.

**Competing explanations still matter:**

- If financially meaningful events are rare for the chosen businesses, the mechanic may be useful but too episodic to justify recurring payment. Revisit ICP or packaging.
- If alerts bring users back but do not affect decisions, the mechanic is anxiety-generating notification theater.
- If customers achieve recurring value but do not convert when the reverse trial changes entitlements, examine paywall and willingness to pay. Do not keep adding prompts.
- If low-quality acquisition produces businesses with no relevant cash-management job, retention tactics cannot repair the channel mix.

**A counterintuitive success condition:** We should be pleased when FinWise sends *fewer* alerts while customers report that important changes are never missed. Silence is part of a trustworthy finance experience.

## 5. What to measure, without rewarding meaningless activity

The uploaded sample engagement scorecard computes **6.7/10** from DAU/MAU (40% × 7), session duration (30% × 3), and feature adoption (30% × 10). Its arithmetic is valid; it is **an illustrative template, not FinWise observed data**. I would not use those weights to steer a cash-management product. They reward time in-product, breadth for its own sake, and potentially repeated anxiety checks.

### Proposed decision-quality scorecard, unscored until data exist

| Dimension | Provisional weight | Operational signal | Why |
| --- | ---: | --- | --- |
| **Depth of value** | 50% | Share of eligible activated businesses that complete a second **verified, decision-dispositioned** review within 28 days | Tests whether a changed-facts return creates substantive value. |
| **Cadence fitness** | 30% | Share of qualifying material changes reviewed within a predeclared decision window, reported with p50/p90 delay and a separate count of unnecessary alerts | Tests timeliness without demanding daily visits. |
| **Decision coverage** | 20% | Share of active target businesses whose saved decisions include the relevant material receivable **and** obligation inputs with acceptable freshness and reconciled exceptions | Broader feature use is only valuable when it closes a consequential blind spot. |

These weights are a **strategic proposal**, not empirically validated scoring coefficients. Do not compress the three metrics into an overall score until event quality, denominator definitions and trade-offs are established. Report them individually first.

**Primary outcome to carry to Module 5:** The proportion of activated businesses that complete a second meaningful financial review within 28 days, counted among **all** activated businesses in a defined start cohort. A meaningful review requires a new or reconsidered decision tied to a source/assumption version and a recorded disposition, not a notification click.

**Diagnostic funnel:** `valid changed event → eligible trigger → notification surfaced → evidence inspected → decision disposition recorded → later paid/retained use`. Track no-event accounts separately; they should not be labeled disengaged because no material event occurred. If experimenting, randomize at the business-account level and distinguish intention-to-treat return use from the descriptive triggered subgroup. Module 5 must settle the actual experimental estimand and sample-size feasibility.

**Guardrails:** false-alert rate, missed material events, stale-data decisions, privacy/consent issues, notifications per account, opt-out rate, decision reversal caused by source corrections, support contacts and time-to-reconcile. Check trial-to-paid conversion, the reverse-trial transition and mature paid retention as lagging commercial signals. The case's **2%** conversion and **40%** one-year paid retention are baseline business facts, not evidence that this mechanic works.

**Kill/redirect decision:** Stop increasing prompt exposure if returns rise but reviewed decisions, accuracy or downstream paid retention do not. Investigate whether the problem is poor sources, excessive interruption, an episodic job, acquisition fit or pricing. Instrument before optimizing.

## 6. The cohort lesson

> **Engagement is not the number of times the customer checks the product. It is the number of consequential moments when the product helps them make a better-informed decision, without making them check unnecessarily.**

That standard is particularly unforgiving in finance. A wrong answer delivered at the right time can destroy trust faster than a right answer delivered too slowly. Module 3 therefore earns the next visit by preserving evidence and customer judgment, not by making the interface addictive.
