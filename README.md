[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)
# Prevent Cash Shortfalls Before They Reach the Payment Date

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Operations--Stage%20Business-orange)

**Designed for consumer goods, wholesale, and manufacturing businesses that need to track committed cash movements, pre-payment obligations, and rolling liquidity before a shortfall occurs.**

[Live Preview](https://hyvoid.github.io/rolling-cashflow-forecast/) · [Purchase Complete Excel](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

Track open order cash commitments, detect liquidity gaps weeks in advance, and maintain a single forward-looking source of truth for short-term cash viability.

---

## Quick Preview

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 03_53_03 PM" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> View the interactive workbook preview: [16-week cash flow demo](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Why This Exists

Most cash shortfalls in growing businesses are not caused by unprofitable operations.

They usually happen because customer pre-payments, milestone receipts, committed purchase orders, and staggered payment terms are difficult to consolidate manually — and standard accounting records are structurally blind to them until an invoice is raised.

The risk is simple:

```
Payment due date arrives
-> Manual bank balance check
-> Prior commitments missed
-> Shortfall discovered at the wire
```

This workbook is designed to change the workflow:

```
New order or supplier PO considered
-> Commitment entered once
-> 16-week cash timeline updated automatically
-> Liquidity gap flagged before it becomes a crisis
```

The commercial problem is not only cash management. It is operational visibility. Finance teams and operators need to know whether the business can cover its next obligation — before agreeing to payment terms.

---

## Three Cash Traps That Catch Growing Businesses

### Trap 1 — Monthly statements misread as a liquidity picture

Standard AR/AP reports reflect what has been invoiced. They do not reflect what has been committed.

A business holding $80,000 in confirmed customer deposits and $60,000 in contracted supplier prepayments due next month shows neither on its income statement until goods move and invoices are raised. The finance team sees a healthy bank balance today. The coming shortfall is invisible.

Finance teams who manage cash from monthly statements routinely work from a picture that is structurally four to six weeks behind reality. The mental model feels complete; the data is not.

### Trap 2 — Pre-payments and purchase orders tracked in separate systems

When the same business takes a 30% customer deposit on Monday and issues a 40% supplier prepayment on Thursday, both transactions affect the same cash pool — but they typically live in different systems, different spreadsheets, or different teams.

Operations that maintain separate tracking for sales commitments and procurement obligations — a natural workflow division — systematically fail to see the net cash position. The regulation does not recognise that operational boundary. Neither does the bank account.

### Trap 3 — Gaps discovered at the payment due date

Manual verification typically happens when a payment falls due or when someone checks the bank account. By the time a gap is identified, the window for action has closed. Reactive responses — emergency credit draws, supplier renegotiations, delayed payroll — carry real cost and real relationship damage.

Pre-gap interception requires that liquidity risk be visible weeks before the obligation matures — which requires all open commitments to be current and all timing calculations to run automatically at the point of planning.

The gap is usually hidden in the relationship between:

- opening cash balance
- deposit and pre-payment receipt timing
- customer balance receipt dates
- supplier payment due dates
- contract payment terms
- order volume and growth rate

That is why manual reconciliation often surfaces the issue late, or misses it entirely.

---

## Who This Tool Is For

| User | Practical Use Case |
|---|---|
| Finance managers | Identify liquidity gaps 6–16 weeks out before they become crises |
| Operations managers | Understand the cash impact of a new order or supplier PO before committing |
| Founders and CEOs | Maintain a single forward view of cash viability as the business scales |
| Procurement teams | Evaluate prepayment demands against actual available liquidity |
| External accountants | Provide short-term cash advisory without building a model from scratch |

Best suited for businesses running mixed customer pre-payment and supplier prepayment structures, where treasury software is cost-prohibitive but manual approaches no longer scale.

---

## What The Workbook Does

### Open Commitment Logging
A single data entry point for all AR, AP, open sales orders, and open purchase orders. Teams enter basic commitment and timing information once; cash timeline calculations run automatically in the background.

### 16-Week Cash Timeline
Automatic mapping of every open commitment to a specific week and cash direction. The rolling window updates each week as new entries are added and prior weeks close out.

### Pre-Decision Liquidity Status
Each week's projected cash balance is visible before a new order is accepted or a new supplier term is agreed. No manual cross-referencing. No day-of-payment discovery.

### Deduplication Logic
Purchase orders already converted to invoices are automatically identified and excluded — ensuring each expected cash movement is counted exactly once and the open-commitment view stays clean.

### Threshold Alert Layer
A minimum safe cash balance is configured by the business. The model highlights which weeks breach the threshold and which specific transactions drive each gap — giving teams a transaction-level diagnostic, not just a red flag.

### Audit-Ready Structure
Every entry is structured and traceable from day one. The full 16-week commitment record can be filtered by direction, counterparty, or week and reviewed without post-processing.

---

## Example Scenario

**Business profile:** Consumer goods importer. Mixed customer pre-payment terms and supplier prepayment requirements. Single finance function.

**The problem:** Each week, the finance manager manually cross-references open sales orders, outstanding customer deposits, pending supplier invoices, and expected goods arrival dates to estimate available cash. Customer commitments are tracked in the CRM. Supplier commitments are tracked in the procurement sheet. Reconciling both into a net cash position takes two hours and produces a view that is already a week stale.

Over one quarter of operations, two liquidity gaps were identified — both within 48 hours of the payment due date.

| | Before | After |
|---|---|---|
| Commitment structure | Two separate sheets, one per team | Single unified workbook |
| Weekly cash check time | ~2 hours across all open positions | Under 5 minutes per week |
| Pre-payment consolidation | Manual cross-reference | Automatic across AR, AP, sales orders, POs |
| Gap discovery | At payment due date; reactive response | 6–8 weeks out; planned response |

**The specific inflection point this tool surfaces:**

A $100,000 customer order carries a 70% balance due before shipment, estimated week 6. The related supplier PO carries a 60% balance due on goods arrival, estimated week 5. Opening cash balance: $10,000.

Week 5 net position: $10,000 − $30,000 = **−$20,000.** Gap exists.
Week 6 net position: −$20,000 + $70,000 = **$50,000.** Resolved.

A monthly view shows the month net-positive. The weekly window shows a real $20,000 shortfall in week 5 that requires action before it arrives — not after.

---

## Why Short-Term Cash Forecasting Works This Way

Rolling cash flow forecasting — direct method, short forward horizon — is a standard treasury discipline maintained by most large corporations as a core operational function. In larger businesses, it is managed by dedicated treasury functions using specialist software.

The direct method works by mapping actual expected cash movements — not accounting entries — to specific dates. Every committed inflow and outflow is translated to a week, a direction, and an amount. The running balance at any point reflects what the business actually expects to hold, not what its accounting records show.

This approach is structurally distinct from:

- **P&L-based cash estimation** — conflates profitability with liquidity; a business can be profitable and illiquid simultaneously
- **Bank balance management** — only reflects what has already moved; committed future outflows are invisible
- **Monthly AR/AP reporting** — excludes pre-invoice commitments entirely; systematically blind to the operational layer

The reason most growing businesses lack this view is not complexity. It is the absence of a structured mechanism to consolidate operational commitments — which live across sales, procurement, and finance — into a single cash timeline.

Useful reference context:
- [AICPA: Direct Method Cash Flow Forecasting](https://www.aicpa.org)
- [AFP: Treasury Management Fundamentals](https://www.afponline.org)

---

## How The 16-Week Window Works

The 16-week window slides forward each week, not each month. Every new entry is mapped to a specific future week based on estimated operational dates and contracted payment terms.

| Operational input | Derived cash event |
|---|---|
| Estimated shipment date + "payment before shipment" term | Customer receipt in the week prior to estimated shipment |
| Estimated goods arrival date + "payment on delivery" term | Supplier outflow in the estimated arrival week |
| Invoice date + "Net 30" term | Customer receipt approximately 4 weeks forward |

**The trap in numbers:**

A business running 10 open orders simultaneously — each with its own deposit structure, balance payment timing, and supplier prepayment schedule — carries upwards of 30 interacting cash events at any given moment. Each event depends on a current operational estimate to remain accurate. Manual consolidation introduces error at each step.

The monthly reset mental model approves positions that the rolling weekly window does not. The calculation is structural, not judgmental. Automation eliminates the error class entirely.

**Why forecast reliability decays at the outer horizon:** The near horizon of weeks 1–8 is populated by commitments already in motion — shipment dates and payment terms that are confirmed or nearly so. Weeks 9–16 depend on operational estimates that may shift materially as orders are placed or delayed. The model is most reliable within the 6–8 week near-horizon. The outer window is directionally useful for planning; it is not a guarantee.

---

## Workbook Logic

The workbook is organized around a practical cash planning workflow:

1. Enter all open AR, AP, sales orders, and purchase orders with estimated dates and payment terms.
2. Apply deduplication to identify and exclude purchase orders already converted to invoices.
3. Map each open commitment to its expected cash week and direction.
4. Calculate the running 16-week balance forward from the opening cash position.
5. Compare each week's projected balance against the minimum safe threshold.
6. Flag gap weeks and identify the specific transactions driving each gap.
7. Preserve the commitment record for weekly rolling review and team communication.

The workbook is intended to be a decision-support and planning tool. It does not replace accounting software, auditable financial records, or professional advice for complex financing decisions.

---

## Purchase

Use the complete Excel workbook here:

[Purchase the complete Excel workbook →](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

---

## Limitations

- **Input dependency** — forecast accuracy is bounded by the quality of data entered; stale shipment estimates or missing commitments produce a false sense of visibility without warning
- **Manual refresh required** — the model does not update automatically; without consistent weekly maintenance, the rolling window degrades and gaps become invisible again
- **Not a system of record** — this is a decision-support layer; it does not replace accounting software, an ERP, or auditable financial records
- **Deterministic, not probabilistic** — each cash event is modelled as a fixed date and fixed amount; payment delay risk, FX movement, and order cancellation scenarios require manual overlay
- **Outer-horizon reliability** — weeks 10–16 depend on operational estimates that may shift materially; the model is most reliable within the 6–8 week near-horizon
- **Multi-currency not modelled** — businesses with significant FX exposure will need to apply exchange rate assumptions as a manual overlay
- **Scale context** — designed for businesses managing 5–50 simultaneous open positions; beyond this range, the manual entry model requires structural adaptation

---

## About This Project

This workbook is part of a broader effort to translate complex operational and financial requirements into lightweight tools that small and medium-sized organizations can actually use.

No ERP. No treasury software subscription. No custom development project.

Just clear business logic, structured data, and repeatable decision support — delivered in software your team already has.

If your operation involves cash management, procurement cycles, or customer billing structures that currently live in someone's head or a disconnected spreadsheet, [see what else is available →](https://www.theseusworkshop.com)

---

## License

Distributed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
