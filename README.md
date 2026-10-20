# FinWise | From first trusted decision to durable paid value

**Product Analytics & Experimentation · Final Project**  
**Chandra Kanojia · October 2026**  
**Role perspective:** Senior Product Manager, financial-management SaaS for small businesses

> **Growth thesis:** FinWise should stop buying more trials into an unproven value loop. Help the right small-business owner reach one **verified financial decision**, make the next consequential review easier, and earn a per-business subscription **only when repeated value and unit economics justify it**.

## Executive judgment

The FinWise case reports **2% trial-to-paid conversion** and **40% one-year paid retention**, while acquisition remains dependent on ads. If those rates apply to the same trial/paid cohorts and observation windows, that is **eight one-year retained payers per 1,000 trials** (`1,000 × 2% × 40%`). This is arithmetic illustrating the scale of commercial leakage, **not** an observed matched cohort or a causal explanation.

We cannot know from those aggregates whether the break is **before first value, at the reverse-trial entitlement boundary, in repeat utility, or in channel fit**. My six-module strategy is therefore a *sequence of falsifiable investment decisions*, not a fabricated retrospective of customer research or a shipped feature.

[**Open the final executive pitch**](./pitch.html) · [**See the interactive decision-first onboarding**](./02-solution/onboarding-prototype.html) · [**Test the Decision Delta wireframe**](./03-mechanic/decision-delta-wireframe.html)

## Six decisions, one economic system

| Module | Product leadership decision | Artifact |
| --- | --- | --- |
| **1 · The Bet** | Start with an owner-operated SMB cash-timing job; prioritize *one trusted decision* over more acquisition. Preserve competing hypotheses. | [Growth thesis and loop](./01-bet/growth-bet.md) |
| **2 · The Solution** | Prototype a verified, scenario-to-decision Aha. The **synthetic** case identifies a day-7 cash-floor breach and a **$10,400** modeled day-11 gap when two invoices are late. | [Activation strategy](./02-solution/activation-solution.md) · [Interactive prototype](./02-solution/onboarding-prototype.html) |
| **3 · The Mechanic** | Earn the next visit through a **Decision Delta** when a material *verified* fact changes; an invoice marked paid is not bank-available cash. | [Engagement mechanism](./03-mechanic/engagement-mechanic.md) · [Interactive wireframe](./03-mechanic/decision-delta-wireframe.html) |
| **4 · The Signals** | Measure **seven-day verified activation**, **28-day decision re-review**, data readiness, paid conversion and paid retention by business cohort. The case supplies no account-level events. | [Data / measurement contract](./04-signals/data-signals.md) |
| **5 · The Validation** | Test decision-first onboarding **only if actual data show pre-value friction**. Business-account randomized A/B; guardrail-first, with 7-day activation as an early metric—not proof of revenue. | [Preregistered experiment brief](./05-validation/experiment-brief.md) |
| **6 · The Model** | Propose transparent **reverse trial → Starter / Owner Plus**, priced per business. **$59/month is a hypothesis to test**, not the known market-clearing price; measure contribution and mature survival. | [Pricing and packaging memo](./06-model/pricing-model.md) |

## The Story

### One friction

**The hardest design choice is refusing to call a plausible financial chart “value.”** A cash forecast can be precise and still wrong for payroll if a receivable is merely marked paid, funds are on hold, the bank's cutoff is earlier than modeled, or payroll taxes have been omitted. The first meaningful activation event therefore needs **reconciled usable evidence, explicit unknowns and an owner-recorded disposition**. That makes a superficially easier onboarding completion metric harder to improve—and a business outcome more credible.

### One Aha

In the illustrative 14-day prototype, an owner starts with **$42,500**, chooses a **$20,000 cash floor**, and sees that when two customers' **$19,500** of receipts are late, cash drops below the floor on **day 7** and reaches **$9,600 on day 11**. The **$10,400** gap converts an abstract dashboard into a concrete question: *“What must I verify or change before the actual payroll cutoff?”* When one **$12,800** receipt is later **simulated as reconciled and available**, the modeled low rises to **$22,400**; when that invoice is only marked paid, the gap **does not change**. The Aha is a **customer-owned, evidence-bounded decision**, not a colored risk score or automatic transfer. These are synthetic calculations, not FinWise customer outcomes.

### What I would take into a product review

1. **Diagnose before shipping.** The case's 2% conversion and 40% retention establish commercial loss, not why it occurs. Audit the account-level funnel, channel mix, reverse-trial terms and data readiness before committing the A/B test.
2. **Treat safety as part of product-market fit.** A false “cash available” reassurance can make a better-looking activation rate economically and ethically worse. Stop unsafe assurance, preserve uncertainty and ensure account-level permission and auditability.
3. **Close the loop through contribution, not engagement theater.** A verified second financial review is an intermediate signal. Durable value is retained **profitable** paying businesses per qualified trial; a hypothetical $59 plan earns the right to exist only through willingness to pay, retention and source/support economics.

## Decision sequence · next 12 months

**0–60 days:** audit trial/paid cohorts, eligibility, financial-evidence failures, entitlement changes and variable economics. Interview owners who never reached value, reached it but declined to pay, and paid then left.  
**60–120 days:** if pre-value friction is material, run the gated onboarding A/B; validate Decision Delta accuracy and the presence of genuine review opportunities.  
**120–240 days:** test Owner Plus packaging and candidate prices **separately** from the onboarding intervention; establish paid cohort contribution.  
**240–365 days:** scale the qualified segment and permissioned distribution only if 90-/365-day survival, account-level contribution and trust guardrails support it. Otherwise, redirect toward the diagnosed cause.

## Evidence standard and how to use the work

- **From the course scenario:** product-market fit, reverse trial, approximately **2%** trial-to-paid conversion, **40%** one-year paid retention, and acquisition concentrated in paid ads.
- **Derived conditional illustration:** **0.8%** durable trial yield / **8 per 1,000**; assumes aligned source cohorts and windows.
- **Designed, not observed:** owner-cash segment choice, the synthetic cash scenarios, onboarding/engagement prototypes, tracking contract, A/B specification, sample-size scenarios, subscription tiers and **$39/$59/$89** pricing anchors.
- **Not supplied:** customer/event-level data, observed behavioral correlations, randomized outcomes, real conversion by segment, production integration readiness, WTP, ARPA, CAC, source fees and contribution margin. No claim of an experiment run, a launched feature or proven monetization is made.

The two standalone prototypes and [`pitch.html`](./pitch.html) are self-contained HTML and use **illustrative data only**; they do not connect to banks, send alerts, or take financial actions.

---

**Submission:** [Repository](https://github.com/iotchandra-afk/finwise-strategy) + [Executive presentation HTML](./pitch.html). Created for Product School's *Product Analytics & Experimentation* six-module FinWise exercise.
