# ArisInfra App Teardown: Product Case Study

*Janvi Nodiyal | Product Management portfolio | B2B construction procurement | November 2026*

## 1. Summary

ArisInfra digitises how Indian real estate and infrastructure developers buy bulk construction materials. This case study maps the buyer journey on ArisInfra's app, benchmarks it against Infra.Market, identifies five friction points, and proposes five features prioritised with RICE. The top pick is turned into a mini PRD with acceptance criteria and success metrics.

**Headline recommendation:** ship one-tap repeat orders first (highest RICE score), then make quotes explainable, because the platform's core promise is one consolidated price.

**Method note:** the analysis is built from public sources (App Store listing, company and press material). Friction points are hypotheses to validate with user interviews (see Section 9).

## 2. Context and scope

**The company.** ArisInfra is a B2B technology-enabled procurement platform founded in 2021. It supplies materials such as steel, cement, aggregates, ready-mix concrete, walling solutions and construction chemicals to developers and contractors. It is asset-light: no warehouses or in-house production, with supply sourced from a vendor network.

**How a quote works.** The platform collects vendor bids and evaluates them on price and credit terms, then shares a single consolidated quotation with the customer.

**Scale signals.** ArisInfra's IPO materials cite about 2,659 customers across 1,075 pin codes. It listed on the Indian exchanges in 2025.

**The app.** The App Store listing describes four modules on one platform:

- **Aris Flow:** business flows and role-based stakeholder management, described as a requirement-to-invoicing platform.
- **Aris Go:** a construction material marketplace for ordering.
- **Aris Delivery:** automated supply chain management with real-time tracking, quality control and compliance.
- **Aris Connect:** a real-time business performance dashboard.

The app was first released in July 2023 and last updated in December 2025, and joining requires contacting the sales team. It does not yet show enough public ratings for an overview, so there is little public user feedback to learn from.

**In scope:** the buyer-side experience (placing a requirement through to invoice). **Out of scope:** the vendor side, ArisInfra's internal tools, pricing strategy and unit economics.

## 3. Users and jobs to be done

These personas are working hypotheses, to be refined by interviews.

| Persona | Job to be done | What success looks like |
|---|---|---|
| Site engineer / procurement executive | "Get the right material to my site on the right day without chasing people." | Requirement raised in minutes, delivery arrives on time and matches the order |
| Project head / purchase manager | "Buy at a defensible price and keep every project in budget." | Clear price justification, spend visibility by project |
| Finance / accounts approver | "Pay the right amount at the right time with clean paperwork." | Credit terms visible, invoices match deliveries |

**Primary persona for this study:** the procurement executive, because they touch every stage of the journey.

## 4. Buyer journey map

| Stage | User goal | What ArisInfra offers (public listing) | Friction hypothesis |
|---|---|---|---|
| 1. Raise requirement | State what is needed, how much, where and when | Aris Flow (requirement to invoicing) | Repeat materials are re-entered each time |
| 2. Get quote | Compare options and find a fair price | Consolidated single quote | Buyer cannot see why this price or what alternatives existed |
| 3. Approve and order | Get internal sign-off, confirm | Role-based stakeholder flows | Approval status may be unclear to the requester |
| 4. Credit and payment | Understand terms and exposure | Credit terms evaluated within bids | Outstanding credit and due dates may not be visible at order time |
| 5. Delivery | Know when material arrives | Real-time tracking | Unclear what happens when a delivery is late or fails quality checks |
| 6. Quality and compliance | Accept or reject material, keep records | Quality control and compliance modules | Rejection and proof-of-delivery steps need to be fast on site |
| 7. Invoice and reconcile | Match invoice to delivery and order | Requirement-to-invoice flow | Mismatches likely resolved offline |
| 8. Monitor and repeat | See spend and plan the next order | Aris Connect dashboard | Dashboard insight may not feed back into reordering |

**Evidence status:** every entry in the last column is a hypothesis from public information, to be confirmed through app walkthroughs and interviews.

## 5. Competitive benchmark

Compared with Infra.Market, the largest player in the space.

| Dimension | ArisInfra | Infra.Market |
|---|---|---|
| Model | Asset-light platform, no warehouses | Aggregates demand and uses manufacturers' spare capacity, with logistics network |
| Catalogue | Steel, cement, aggregates, RMC, walling, chemicals | Much broader: concrete, steel, tiles, bath fittings, paints, plumbing, electricals and more |
| Pricing | Vendor bids consolidated into one quote | Wholesale pricing from aggregated demand |
| Credit | Credit terms part of bid evaluation | Credit or financing positioned as core to the offer |
| Delivery | Real-time tracking, quality control | Delivery tracking and order updates from order to site |
| Analytics | Aris Connect dashboard | Not assessed |

**Takeaway:** ArisInfra competes on procurement intelligence and workflow depth rather than catalogue breadth. That makes quote clarity and workflow speed the right places to win.

## 6. Friction points

Each is a hypothesis with a way to test it.

1. **The single quote is a black box.** Procurement managers must justify prices to finance. If the app shows one number with no rationale, buyers may re-negotiate offline or distrust it. *Test:* ask 3 buyers how they would defend this price internally.
2. **Repeat orders start from scratch.** Steel and cement are bought again and again for the same sites. *Test:* count how many fields a repeat requirement needs versus a first order.
3. **Credit position is not visible at the moment of ordering.** Credit terms drive vendor choice, but exposure and due dates may live elsewhere. *Test:* ask what buyers check before confirming an order.
4. **Delivery exceptions lack a clear workflow.** Tracking shows where a truck is, but a late or rejected load needs fast escalation and proof. *Test:* ask for the last bad delivery and walk through what happened.
5. **Onboarding is sales-led and the module names are opaque.** "Flow", "Connect", "Go" and "Delivery" do not say what task each solves, and there is no public rating loop. *Test:* ask a new user to find where to place an order, unaided.

## 7. Feature proposals and prioritisation

**RICE** = Reach x Impact x Confidence / Effort. Reach is scored 1-10 (share of buyers affected per quarter). Impact is 0.25-3. Effort is in person-months. **These scores are illustrative assumptions and should be replaced with interview and data evidence.**

| # | Feature | Reach | Impact | Confidence | Effort | RICE |
|---|---|---|---|---|---|---|
| B | One-tap repeat orders and saved requisition templates | 7 | 2 | 80% | 1.5 | **7.5** |
| A | "Why this price" quote panel (vendor count, price vs market range, credit terms) | 8 | 2 | 70% | 2 | **5.6** |
| C | Credit and payment timeline shown at order confirmation | 6 | 2 | 60% | 2 | **3.6** |
| D | Delivery exception workflow (delay alerts, reject-with-photo, auto-escalation) | 5 | 3 | 60% | 3 | **3.0** |
| E | LLM-assisted order intake (paste a BOQ or message, get a structured requisition for review) | 7 | 2 | 50% | 3 | **2.3** |

**Why E ranks last but still matters:** it scores low on confidence and effort today, but it is the most direct use of AI-assisted workflows and worth a prototype once B and A are shipped. Extraction errors would cost real money, so it needs a human-review step.

## 8. Roadmap and mini PRD

**Now (0-6 weeks):** B, one-tap repeat orders.
**Next (6-12 weeks):** A, quote explainability; C, credit timeline.
**Later (quarter 2):** D, delivery exceptions; E, LLM order intake prototype behind a feature flag.

### Mini PRD: One-tap repeat orders

**Problem.** Procurement executives re-enter the same material, specification and site details for recurring purchases, which wastes time and introduces errors.

**Goal.** Cut the time to raise a repeat requirement and reduce order-entry mistakes.

**User stories**
- As a procurement executive, I want to reorder a past requirement in one tap so that I do not retype specs.
- As a procurement executive, I want to save a requirement as a template for a site so that weekly materials are ready to go.
- As a purchase manager, I want to see which orders came from templates so that I can spot-check quantities.

**Acceptance criteria**
- Given a delivered order, when the user taps Reorder, then a new draft requisition opens with material, grade, site and unit prefilled and quantity and delivery date left editable.
- Given a draft from a template, when the user submits, then it follows the same approval flow as a new requisition.
- Given a material is no longer available, when a template loads, then the item is flagged and the user is offered the closest alternative.
- Given an order created from a template, then it is tagged so that approvers can see its origin.

**Success metrics**
- *Primary:* share of requisitions created via Reorder or templates (target to be set after baseline).
- *Efficiency:* median time from opening the app to submitting a repeat requisition.
- *Guardrails:* order edit and cancellation rate after submission, quote-to-order conversion, quantity-error support tickets.

**Funnel to instrument:** requirement started, requirement submitted, quote received, quote accepted, delivered, invoiced. Segment by new versus repeat orders.

**Out of scope (v1).** Automatic scheduling of recurring orders, cross-site templates, and price locking.

**Risks.** Stale specs ordered unintentionally (mitigate with an editable review screen and an expiry on templates); approval bypass (mitigate by reusing the existing flow).

**Rollout.** Pilot with a small group of repeat-heavy accounts, compare against a control group for 4 weeks, then widen.

## 9. Validation plan

**Interviews (aim for 5, 20 minutes each).** Procurement executives, site engineers or purchase managers.

1. Walk me through the last time you ordered steel or cement. What did you do first?
2. What information did you need before you were comfortable confirming the price?
3. How do you handle repeat orders for the same site?
4. Tell me about your last late or rejected delivery. What happened next?
5. What do you check on credit and payment before you place an order?

**Usability test (3 tasks, think aloud).** Place a first order; reorder a past order; find your outstanding credit. Record time, errors and where people hesitate.

**What would change my mind.** If buyers say the quote is already trusted and rarely questioned, drop A in priority. If repeat orders are already quick, B falls and C or D move up.

## 10. Limitations

- Built from public information. Company-internal data (conversion, retention, support tickets) is not available.
- The app is gated for onboarded customers, so screens and flows could not be fully observed. Findings about in-app behaviour are hypotheses.
- RICE inputs are assumptions, not measurements.

## 11. Sources

- Apple App Store listing, ArisInfra: https://apps.apple.com/pg/app/arisinfra/id6453520656
- Inc42 on ArisInfra's FY24 results and bid-aggregation model: https://inc42.com/?p=474170
- IPO Central, ArisInfra IPO review: https://ipocentral.in/arisinfra-solutions-ipo-review/
- Inc42 on ArisInfra's anchor round and competitors: https://inc42.com/buzz/arisinfra-raises-inr-225-cr-from-anchor-investors
- Inc42 on Infra.Market's Series D: https://inc42.com/?p=259139
- Indian Cement Review, interview with Infra.Market's retail head: https://indiancementreview.com/2022/03/01/we-are-digitising-the-entire-value-chain/amp
