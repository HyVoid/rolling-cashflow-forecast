[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# 16-Week Rolling Cash Flow Forecast Excel Template: Direct-Method Liquidity Planner, PO Commitment Tracker & Working Capital Model

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Focus](https://img.shields.io/badge/focus-Working%20Capital%20%26%20Treasury-orange)

**A direct-method 16-week rolling cash flow forecast spreadsheet built in Microsoft Excel for wholesale, import/export, e-commerce inventory, and manufacturing businesses managing open purchase orders (POs), supplier prepayments, customer deposits, and short-term working capital.**

[Launch Interactive 16-Week Rolling Cash Flow Simulator Demo](https://hyvoid.github.io/rolling-cashflow-forecast/) ·

[Download the Complete 16-Week Rolling Cash Flow Excel Workbook](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)

</div>

**16-Week Rolling Cash Flow Forecast Workbook** is an automated **Microsoft Excel short-term liquidity planner** and **open commitment cash tracker**. Extending beyond standard **13-week cash flow models** to cover full 110-day inventory and production lead times, it consolidates **Accounts Receivable (AR)**, **Accounts Payable (AP)**, **unbilled Sales Orders (SO)**, and **committed Purchase Orders (PO)** into a single weekly cash timeline—flagging working capital shortfalls and minimum cash buffer breaches weeks before payment due dates.

---

## Visual Preview: 16-Week Cash Timeline & Threshold Alert Dashboard

<img width="1672" height="941" alt="16-Week Rolling Cash Flow Forecast Excel Template showing weekly cash inflows, supplier PO prepayments, net liquidity balance, and shortfall alerts" src="https://github.com/user-attachments/assets/d43699bc-4a15-470c-901e-7b372c953861" />

> Test the weekly commitment mapping and liquidity threshold alerts in your browser: [Interactive 16-Week Direct-Method Cash Flow Forecast Demo](https://hyvoid.github.io/rolling-cashflow-forecast/)

---

## Why Accrual Accounting Fails to Prevent Short-Term Cash Shortfalls

Profitable wholesale, manufacturing, and physical product businesses routinely experience acute liquidity crunches during growth phases. These cash shortfalls happen because **customer deposits**, **milestone progress billings**, **contracted supplier prepayments**, and **staggered Net 30/60/90 payment terms** occur weeks before an accounting invoice is ever posted to the general ledger.

**The Reactive Bank-Balance & AR/AP Workflow (High Default Risk):**

```text
Supplier wire due date arrives
-> Finance checks current bank balance and billed AP aging
-> Unbilled PO prepayments and freight commitments overlooked
-> Working capital shortfall discovered 48 hours before wire deadline

```

**The Proactive 16-Week Commitment Forecasting Workflow (Pre-Decision Control):**

```text
New customer order or supplier Purchase Order (PO) proposed
-> Prepayment and balance milestones logged once in the commitment ledger
-> 16-week rolling cash flow timeline updates automatically
-> Liquidity gap and minimum buffer breach flagged 6–12 weeks in advance

```

Finance managers, controllers, and operations leads need pre-decision liquidity visibility. Before signing a supplier purchase order or granting Net 60 terms to a wholesale buyer, operators must verify that the weekly cash trough remains above the company's minimum operating cash reserve.

---

## The Business Logic & Methodology: Direct-Method Commitment Forecasting

This workbook solves the **pre-invoice working capital blindness problem** by combining **Direct-Method Rolling Cash Flow Forecasting** with **Order-to-Invoice Commitment Deduplication**.

### The Commercial Problem: The Accrual-to-Cash Timing Gap in Physical Supply Chains

Standard accounting software (QuickBooks, Xero, NetSuite GL) recognizes financial events only when an **Invoice** or **Bill** is issued. However, in manufacturing, wholesale distribution, and import operations, cash is legally committed at the **Order Layer**:

1. **Procurement Cash Outflows:** A factory requires a 30% deposit upon Purchase Order (PO) issuance and a 70% balance upon Bill of Lading (B/L) or warehouse arrival—weeks before a formal AP vendor bill is booked.
2. **Sales Cash Inflows:** A B2B customer pays a 25% deposit upon Sales Order (SO) confirmation and the remaining 75% either before shipment or on Net 30/60 terms after delivery.
3. **Why 16 Weeks Beats Standard 13-Week Models:** A standard corporate 13-week (90-day) cash forecast cuts off right before a 60-day production run plus 30-day ocean transit plus Net 30 customer collection clears. Expanding the rolling window to **16 weeks (112 days)** captures the entire cash conversion cycle from initial PO deposit to final customer collection.

### The Core Methodology: Three-Stage Deterministic Cash Mapping

Instead of projecting cash from top-line P&L averages, the workbook executes a deterministic three-stage calculation across a sliding 16-week window ($t \in [1, 16]$):

1. **Commitment-to-Invoice Deduplication Engine:**

$$\text{Active Cash Events} = \{ \text{Billed AR} \} \cup \{ \text{Billed AP} \} \cup \{ \text{Open SOs} \setminus \text{Invoiced SOs} \} \cup \{ \text{Open POs} \setminus \text{Billed POs} \}$$



*Business Effect:* Once a Purchase Order converts into a formal vendor invoice in your accounting system, the deduplication flag excludes the original PO line so the cash outflow is never double-counted.
2. **Milestone Date-Offset Translation:**
Every active commitment is decomposed into discrete cash tranches (e.g., Deposit Tranche + Balance Tranche) mapped to target calendar weeks based on operational trigger dates (Order Date, Estimated Shipment Date, Estimated Arrival Date, or Invoice Date) plus contracted payment terms ($\Delta \text{Days}$).
3. **Rolling Weekly Liquidity & Buffer Breach Evaluation:**

$$\text{Ending Cash}_{w} = \text{Opening Cash}_{w} + \sum \text{Committed Inflows}_{w} - \sum \text{Committed Outflows}_{w}$$


$$\text{Liquidity Variance}_{w} = \text{Ending Cash}_{w} - \text{Minimum Safe Cash Threshold}$$



*Business Effect:* Any week where $\text{Ending Cash}_{w} < \text{Minimum Safe Cash Threshold}$ triggers an immediate visual alert and isolates the exact PO or delayed AR line item causing the working capital trough.

---

## Three Working Capital Traps in Manual Cash Flow Spreadsheets

### Trap 1: Relying on Monthly P&L and Billed AR/AP Aging Reports for Liquidity

Standard Accounts Receivable and Accounts Payable aging reports only display **invoiced transactions**.

Consider an importer holding $80,000 in unbilled customer order deposits and facing $60,000 in contracted factory balance payments upon container arrival next month. Neither obligation appears on the P&L or standard AP aging report until inventory lands and vendor bills are entered. Managing weekly treasury from monthly accrual statements leaves the finance team four to six weeks behind real cash commitments.

### Trap 2: Siloed Tracking Between Sales Orders (CRM) and Purchase Orders (Procurement)

When the sales team accepts a 30% customer deposit on Monday and the purchasing team commits to a 40% supplier prepayment on Thursday, both actions draw from the same operating bank account. Yet in most SMEs, sales commitments live in a CRM or order sheet while supplier POs live in a separate procurement tracker.

Maintaining disconnected spreadsheets for customer inflows and supplier outflows prevents operators from seeing the **net weekly cash position** when fulfillment dates slip by even one week.

### Trap 3: Intra-Month Cash Troughs Hidden Inside Positive Monthly Totals

A monthly cash flow summary can show a healthy positive net cash balance at month-end while hiding a fatal multi-day overdraft in Week 2 or Week 3.

Weekly cash shortfalls emerge from the timing mismatch between six operational variables:

* Opening operating bank balance
* Customer deposit and milestone receipt dates
* Final customer balance collection terms (e.g., Prior to Shipment vs. Net 30)
* Supplier PO prepayment and goods-on-arrival wire dates
* Freight, duty, and customs clearance outlays
* Order volume acceleration during peak seasonal builds

Mapping every commitment to a specific 7-day bucket exposes intra-month cash troughs while you still have 6 to 10 weeks to negotiate supplier terms, accelerate customer collections, or draw on a revolving line of credit.

---

## Who This 16-Week Rolling Cash Flow Excel Template Is For

Designed for operational finance teams and business owners who need **direct-method treasury forecasting inside Microsoft Excel** without enterprise TMS software costs:

| Role & Search Persona | Specific Operational Scenario & Template Use Case |
| --- | --- |
| **Finance Managers & Controllers** *(16-Week / 13-Week Cash Flow Forecast Excel Template)* | Replace manual Friday bank reconciliations with a rolling 16-week direct-method liquidity forecast that flags cash buffer breaches 6–12 weeks ahead. |
| **Supply Chain & Operations Directors** *(Purchase Order Cash Flow & Prepayment Tracker)* | Simulate the exact weekly cash impact of placing a large seasonal factory PO or delaying a shipment date before signing supplier contracts. |
| **Inventory-Heavy Founders & CEOs** *(Working Capital & Runway Forecast Spreadsheet)* | Maintain a single forward-looking dashboard of net operating liquidity across rapid SKU expansion, wholesale fulfillment, and inventory build cycles. |
| **Procurement & Purchasing Leads** *(Supplier Deposit & Payment Terms Planner)* | Evaluate vendor prepayment demands (e.g., 30/70 vs. 50/50 split terms) against actual projected weekly cash availability. |
| **Fractional CFOs & Advisory CPAs** *(Short-Term Treasury & Turnaround Cash Model)* | Deploy a standardized, audit-ready weekly cash flow control tool for SME clients facing tight working capital or lender reporting covenants. |

---

## Real-World Use Cases: Solving Pre-Invoice Working Capital & Liquidity Scenarios

### Scenario A: Import/Export & Wholesale Distributors Managing 30/70 Factory Prepayments

Importers routinely pay 30% upon PO placement and 70% upon Bill of Lading or port arrival, while wholesale retail buyers pay Net 30 or Net 60 after warehouse delivery. By logging open POs and wholesale SOs into the **16-Week Cash Timeline**, the controller sees the exact 4-to-8 week working capital trough between paying the overseas factory and collecting from the domestic retailer.

### Scenario B: Contract Manufacturers & Custom Equipment Builders Tracking Milestone Billing

Manufacturers running multi-stage builds collect customer progress payments (e.g., 40% deposit, 30% on sub-assembly, 30% prior to dispatch) while purchasing raw materials upfront. When a production milestone slips by two weeks, updating the estimated shipment date in the workbook automatically shifts the downstream customer cash inflow and reveals whether raw material payables will breach the minimum cash reserve.

### Scenario C: Fractional CFOs Running Weekly Cash War-Rooms & Lender Covenant Reporting

During working capital turnarounds or seasonal credit-line draws, banks and leadership teams require a transparent weekly direct cash forecast (often requested as a 13-week or 16-week rolling cash flow report). This template provides transaction-level drill-downs showing exactly which customer invoices and vendor POs drive each week's net cash flow.

---

## What The Workbook Tracks: Pain-Point to Solution Mapping

| Treasury & Cash Management Pain Point | High-Frequency Search Requirement | Built-In Excel Workbook Solution |
| --- | --- | --- |
| **Unbilled POs Missing from Cash Forecasts** | *How to include open purchase orders in cash flow forecast Excel* | **Unified Open Commitment Ledger:** Captures billed AR, billed AP, unbilled Sales Orders, and open Purchase Orders in one structured input table. |
| **Double-Counting POs After Invoicing** | *Prevent duplicate PO and invoice entries in cash projection* | **Automated PO-to-Invoice Deduplication:** Identifies and excludes purchase orders that have already converted into formal AP invoices so every dollar is counted once. |
| **Intra-Month Overdrafts & Surprise Shortfalls** | *Weekly rolling cash flow forecast template with low-cash alerts* | **Configurable Threshold Alert Layer:** Compares projected weekly ending cash against your custom Minimum Safe Cash Balance and highlights breach weeks in real time. |
| **Stale Shipment & Delivery Estimates** | *Dynamic cash flow model based on shipment dates and payment terms* | **Automated Term-to-Week Mapping:** Translates operational dates (Estimated Ship Date, Arrival Date, Invoice Date) and payment terms into exact weekly cash buckets. |
| **Slow Pre-Commitment Approval Checks** | *Test cash impact of new supplier purchase order before buying* | **Pre-Decision Liquidity Sandbox:** Enter a proposed PO or customer order to see immediately whether the new commitment creates a cash deficit 6–16 weeks out. |

---

## Case Study: Monthly Accrual Blindness vs. 16-Week Rolling Cash Visibility

**Business Profile:** Consumer goods importer managing $2M–$10M in annual turnover, operating with mixed customer deposit terms, overseas supplier prepayment schedules, and a lean single-manager finance team.

**The Operational Breakdown:** Every week, the finance manager spent two hours cross-referencing CRM sales orders, customer deposit receipts, open factory POs, and freight arrival schedules across disconnected spreadsheets. Despite showing positive monthly net cash flow on paper, the business suffered two emergency cash shortfalls in a single quarter—both discovered less than 48 hours before international supplier wires were due.

### Comparison: Disconnected AR/AP Spreadsheets vs. Automated 16-Week Commitment Model

| Treasury Operation | Manual Disconnected Spreadsheets (Before) | Automated 16-Week Rolling Cash Flow Workbook (After) |
| --- | --- | --- |
| **Commitment Data Architecture** | Siloed CRM sales sheets, procurement PO trackers, and accounting AR/AP exports | **Single unified commitment ledger** covering AR, AP, Open SOs, and Open POs with deduplication |
| **Weekly Forecast Preparation Time** | ~2 hours of manual VLOOKUPs and date cross-referencing every Friday | **Under 5 minutes per week**; rolling 16-week window updates dynamically upon date entry |
| **Pre-Invoice Prepayment Visibility** | Blind to supplier deposits and milestone balances until vendor bills are booked | **Full milestone mapping** across deposit tranches, pre-shipment payments, and delivery wires |
| **Liquidity Shortfall Detection Window** | Discovered 24–48 hours before wire due date (forced emergency credit draws) | **Flagged 6–12 weeks in advance** via automated minimum cash threshold breach alerts |

### The Exact Inflection Point This Workbook Surfaces

Consider a **$100,000 Customer Sales Order** and its linked **$50,000 Supplier Purchase Order** starting from an **Opening Cash Balance of $10,000**:

* **Supplier PO Balance ($30,000 outflow):** 60% due upon goods arrival in **Week 5**.
* **Customer SO Balance ($70,000 inflow):** 70% due prior to warehouse dispatch in **Week 6**.

| Reporting Granularity | Week 5 Net Cash Position | Week 6 Net Cash Position | Operational Conclusion |
| --- | --- | --- | --- |
| **Traditional Monthly Cash Summary** | *Hidden inside monthly total* | **+$50,000 Month-End Cash** | False green light; finance approves terms without seeing the mid-month default |
| **16-Week Rolling Weekly Model** | **−$20,000 Cash Shortfall** ($10K − $30K) | **+$50,000 Recovery** (−$20K + $70K) | **Flags the $20,000 Week 5 deficit 5 weeks early**, allowing the team to align supplier wire terms with customer receipt |

---

## Treasury Standards Behind Direct-Method Rolling Cash Forecasting

Corporate treasury teams rely on **short-term direct-method rolling cash flow forecasting** because accrual income statements measure profitability rather than cash solvency. Rapidly growing product businesses frequently generate strong accounting margins while running out of operating cash due to inventory prepayment timing.

The direct method bypasses accrual accounting adjustments and maps **100% of expected gross cash receipts and gross cash disbursements** to specific weekly buckets:

| Traditional Reporting Method | Structural Limitation in Operations | How the 16-Week Direct-Method Model Solves It |
| --- | --- | --- |
| **Indirect P&L Cash Estimation** | Conflates accounting net income with liquid bank funds; hides mid-month working capital spikes | Maps **actual dated cash receipts and wire disbursements** week by week |
| **Daily Bank Balance Checking** | Purely backward-looking; shows settled cash while ignoring $100K+ in committed upcoming PO wires | Projects **forward running cash balances** across the next 16 consecutive weeks |
| **Monthly AR / AP Aging Reports** | Excludes unbilled purchase orders and pre-shipment customer milestones | Integrates **pre-invoice order commitments** alongside billed receivables and payables |

**Authoritative Treasury & Cash Management Frameworks Referenced:**

* [AICPA: Direct Method Cash Flow Forecasting & Working Capital Management](https://www.aicpa-cima.com)
* [Association for Financial Professionals (AFP): Short-Term Treasury & Rolling Cash Forecasting Standards](https://www.afponline.org)

---

## How the 16-Week Rolling Horizon & Date-Offset Mapping Work

The 16-week forecast horizon rolls forward week by week. Every open order or invoice is assigned to a specific future cash week by combining its **operational milestone date** with its **contracted payment term**:

| Operational Milestone Input | Contracted Payment Term | Derived Weekly Cash Flow Event in Model |
| --- | --- | --- |
| **Estimated Customer Shipment Date** | *Balance Due Prior to Shipment* | **Cash Inflow (Receipt)** mapped to the week immediately preceding estimated shipment |
| **Estimated Goods Arrival Date (ETA)** | *Balance Due on Delivery / Arrival* | **Cash Outflow (Supplier Wire)** mapped to the estimated warehouse/port arrival week |
| **Customer Invoice Issue Date** | *Net 30 Days Credit Term* | **Cash Inflow (Receipt)** mapped 4 weeks forward from invoice date |

**Why Forecast Precision Splits Between the Near Horizon (Weeks 1–8) and Outer Horizon (Weeks 9–16):**

* **Weeks 1–8 (High-Confidence Execution Window):** Driven by confirmed invoices, locked vessel schedules, and active purchase orders already in production. Used for hard payment scheduling, wire approvals, and credit-line draw decisions.
* **Weeks 9–16 (Strategic Planning & Procurement Window):** Driven by estimated production lead times and pipeline sales orders. Used to stress-test whether new supplier POs can be funded from internal cash flow before contracts are signed.

---

## Quick Start Tutorial: How to Build Your 16-Week Rolling Cash Flow Forecast in 7 Steps

Follow this step-by-step workflow to transition your finance and operations team from reactive bank-balance checks to proactive 16-week liquidity management:

1. **Test Commitment Scenarios in the Interactive Browser Demo**
Open the [Interactive 16-Week Rolling Cash Flow Web Simulator](https://hyvoid.github.io/rolling-cashflow-forecast/) to explore how open POs, customer deposits, and shipment delays shift weekly cash balances in real time.
2. **Configure Opening Cash Balance and Minimum Safe Cash Buffer**
Enter your current operating bank balance, define your starting Monday forecast date, and set your company's **Minimum Safe Cash Threshold** (e.g., $25,000 or 1 month of fixed payroll/opex).
3. **Log Billed Accounts Receivable (AR) and Accounts Payable (AP)**
Input outstanding customer invoices and vendor bills with their contracted due dates to establish your baseline post-invoice cash timeline.
4. **Enter Unbilled Sales Orders (SO) and Open Purchase Orders (PO)**
Record confirmed customer orders and active supplier POs along with deposit percentages, balance percentages, estimated shipment/arrival dates, and payment terms.
5. **Run Automated PO-to-Invoice Deduplication**
Mark or link purchase orders that have already been billed by suppliers so the deduplication engine excludes them from open commitments and prevents double-counting.
6. **Inspect Weekly Threshold Breach Alerts and Diagnose Cash Troughs**
Review the 16-week cash timeline to spot any week falling below your minimum buffer, then filter the commitment table by that week number to identify the exact supplier PO or delayed customer collection driving the gap.
7. **Standardize Your Weekly Cash Review with the Reusable Excel Workbook**
Once you have tested the logic in the single-session web preview, **[Download the Complete, Reusable 16-Week Rolling Cash Flow Excel Template](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)** to save your ongoing company data, customize counterparty tracking, and run your weekly 5-minute liquidity review offline in Microsoft Excel.

*Disclaimer: This workbook is an operational cash planning and decision-support model. It supplements—rather than replaces—formal GAAP/IFRS accounting software, audited financial statements, and licensed treasury or financing advice.*

---

## Download the Complete Excel Template

Ready to eliminate surprise payment-date shortfalls and unify your AR, AP, and open order commitments in one rolling timeline?

👉 **[Get the Complete 16-Week Rolling Cash Flow Forecast Excel Workbook](https://www.theseusworkshop.com/l/16wcashflow?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=rolling-16-week-cashflow)**

---

## Technical Scope & Operational Limitations

* **Data Freshness Dependency:** Forecast accuracy relies on current operational estimates; unlogged supplier POs or outdated freight arrival dates will understate or misalign weekly cash outflows.
* **Weekly Rolling Maintenance Cadence:** Designed for a 5-minute weekly refresh (updating opening cash, rolling the start date forward, and adjusting shifted shipment ETAs).
* **Decision-Support Layer (Not an Accounting GL):** Built for forward-looking liquidity planning; does not replace ERP systems, double-entry bookkeeping software, or statutory tax records.
* **Deterministic Date Mapping:** Models each commitment tranche on a specific target date and amount; probabilistic late-payment haircuts or order cancellation stress-tests require manual date/amount overrides.
* **Outer-Horizon Variance (Weeks 9–16):** Weeks 1–8 reflect near-locked commitments, whereas Weeks 9–16 reflect operational estimates subject to supply chain lead-time shifts.
* **Single Base Currency Architecture:** Multi-currency supplier POs (e.g., USD vs. EUR/CNY) should be entered at your budgeted or forward-hedged exchange rate in the base currency.
* **Recommended Operational Scale:** Optimized for SMEs actively managing **5 to 50 concurrent open orders/POs** per rolling cycle in Microsoft Excel.

---

## Other Tools in This Series

* **[Multi-Currency-Trade-Financial-Analyzer](https://github.com/HyVoid/Multi-Currency-Trade-Financial-Analyzer)** — Which trade flows are actually profitable after currency effects? — Measure multi-currency trade profitability across cross-border operations.
* **[RTL_Loan_Sizer_Pricer](https://github.com/HyVoid/RTL_Loan_Sizer_Pricer)** — What financing structure is supportable under different borrower and collateral scenarios? — Compare lending scenarios using risk-adjusted financing assumptions.
* **[Personal-Business-Dual-Track-Budget-Manager](https://github.com/HyVoid/Personal-Business-Dual-Track-Budget-Manager)** — Where is personal and business cash being mixed or misallocated? — Separate personal and business cash flows into independently tracked budget tracks.
* **[Multifamily-Value-Add-Acquisition-Model](https://github.com/HyVoid/Multifamily-Value-Add-Acquisition-Model)** — Does this real estate acquisition still create equity value after renovation and operating assumptions? — Evaluate multifamily acquisition returns under renovation financing and operating scenarios.
* **[Real-Estate-Valuation-all-in-one-calculator](https://github.com/HyVoid/Real-Estate-Valuation-all-in-one-calculator)** — What is a property worth under different valuation methods? — Calculate property value across multiple valuation methods with tax and capital expenditure modeling.
* **[multi-entity-expense-allocation](https://github.com/HyVoid/multi-entity-expense-allocation)** — Are shared costs being allocated fairly across entities or are some assets overburdened while others escape their true cost exposure? — Distribute supplier invoices across multiple legal entities and operating assets using configurable allocation methodologies.
* **[investment-pool-nav-excel-template](https://github.com/HyVoid/investment-pool-nav-excel-template)** — What is each participant actually owed based on their entry timing and current pool value? — Track investment pool ownership continuously using NAV-based unit accounting.
* **[shopify-cash-flow-forecast-excel-toolkit](https://github.com/HyVoid/shopify-cash-flow-forecast-excel-toolkit)** — Which operational commitments will create a cash problem in the next twelve weeks? — Connect Shopify sales bank transactions advertising spend and inventory purchasing into a unified cash flow decision framework.
* **[Revenue-Management-Decision-Engine](https://github.com/HyVoid/Revenue-Management-Decision-Engine)** — Has enough meaningful information changed to justify a pricing adjustment? — Govern pricing recommendations through configurable guard rails that prevent unnecessary revenue volatility.
* **[amazon-wbr-sqp-analytics-template](https://github.com/HyVoid/amazon-wbr-sqp-analytics-template)** — What actually changed in the business this period and which products or keywords drove the change? — Transform Amazon Seller Central SQP and Sellerboard exports into standardized executive business reviews.
* **[food-manufacturing-cost-calculator-excel](https://github.com/HyVoid/food-manufacturing-cost-calculator-excel)** — Which products are actually profitable after all manufacturing costs are allocated and which are destroying margin? — Allocate factory labor utilities overhead and material costs to every SKU for true unit manufacturing economics.
* **[ecommerce-profit-calculator-excel](https://github.com/HyVoid/ecommerce-profit-calculator-excel)** — Which orders are actually profitable after all hidden costs and where is money leaking across channels and currencies? — Reconstruct true order-level profitability by reconciling sales payouts shipping costs payment fees and marketplace commissions across multi-channel e-commerce operations.
* **[construction-job-costing-excel-template](https://github.com/HyVoid/construction-job-costing-excel-template)** — Which contractor projects and customers are actually profitable after all job costs? — Connect lead estimation, job execution, and actual cost tracking into a unified contractor profitability framework.
* **[Flora-Pastry-Coffee-Shop-Operating-Control-System](https://github.com/HyVoid/Flora-Pastry-Coffee-Shop-Operating-Control-System)** — Is the shop genuinely profitable after all ingredient, labor, and operating costs? — Connect recipe costing, sales, inventory consumption, and operating expenses into a unified profitability and cash flow framework.
* **[freight-forwarder-job-costing-excel](https://github.com/HyVoid/freight-forwarder-job-costing-excel)** — Which freight bookings are actually profitable after all costs, fees, and currency conversion? — Measure booking-level freight profitability by reconciling revenue, COGS, bank fees, and container costs across mixed-currency transactions.
* **[cross-entity-logistics-console](https://github.com/HyVoid/cross-entity-logistics-console)** — Which containers and customers are actually profitable across customs and fleet operations? — Consolidate customs clearance and fleet execution data into a single container-level profitability view.
* **[family-loan-tracker-excel](https://github.com/HyVoid/family-loan-tracker-excel)** — What is actually owed today after years of transfers and accrued interest? — Reconcile long-term fund transfers and interest accruals into a current outstanding balance.
* **[3-statement-financial-model-excel](https://github.com/HyVoid/3-statement-financial-model-excel)** — What will our financial statements look like under different operating and financing scenarios? — Forecast integrated financial statements by linking revenue, expenses, working capital, and debt into a unified model.
* **[assisted-living-cost-allocation-excel](https://github.com/HyVoid/assisted-living-cost-allocation-excel)** — How much of each building's reported margin is actually generated by that building versus by the way corporate costs were allocated? — Allocate shared expenses across operating units while preserving source transactions and reconciling unit-level results to company totals.
* **[real-estate-development-feasibility-excel](https://github.com/HyVoid/real-estate-development-feasibility-excel)** — At what maximum land acquisition price does this development project become a bankable investment? — Evaluate residential development opportunities by screening land comparables, estimating construction costs, and calculating profit-on-cost thresholds.
* **[uk-residential-costing-software](https://github.com/HyVoid/uk-residential-costing-software)** — Will this construction project actually hit its target margin once site logistics, waste factors, and trade rate changes are accounted for? — Separate physical building quantities from volatile trade rates and site preliminaries to cascade commercial markups across tender budgets and client quotations.
* **[b2b-pricing-landed-cost-excel-model](https://github.com/HyVoid/b2b-pricing-landed-cost-excel-model)** — Which wholesale prices and customer segments actually preserve margin once freight, duties, payment terms, and FX are fully costed? — Calculate SKU-level landed costs, cost-to-serve, and pocket-margin price waterfalls to simulate cross-border wholesale profitability.
* **[custom-label-pricing-calculator](https://github.com/HyVoid/custom-label-pricing-calculator)** — What should we charge for a custom label order at each quantity tier to stay competitive and profitable? — Calculate parametric label pricing by modeling substrate square-inch costs, setup charges, and quantity-tier discount breaks against competitor benchmarks.
* **[landed-cost-calculator-retail-deduction-excel](https://github.com/HyVoid/landed-cost-calculator-retail-deduction-excel)** — What is the true net margin on each SKU once actual landed costs and retailer deductions are accounted for? — Reconcile PO-estimated landed costs against actual freight, duty, FX, and drayage charges while auditing retailer remittance deductions to expose SKU-level net margin.
* **[saas-finance-mrr-burn-rate-excel](https://github.com/HyVoid/saas-finance-mrr-burn-rate-excel)** — Can we make this week's hiring, marketing, and vendor commitments without running out of cash before the books close? — Track weekly cash burn pacing, MRR/ARR waterfall variance, retention metrics, and payroll costs against budget before month-end close.
* **[startup-financial-model-excel](https://github.com/HyVoid/startup-financial-model-excel)** — Will our growth plan run out of cash before cohort monetization catches up? — Forecast multi-year cash burn, runway, unit economics, and fundraising dilution from bottom-up cohort and headcount assumptions.
* **[shopify-pnl-reconciliation-excel](https://github.com/HyVoid/shopify-pnl-reconciliation-excel)** — Is each Shopify storefront actually profitable once true SKU-level costs, shared expenses, and bank charges are reconciled? — Reconcile multi-store Shopify sales exports against SKU-level COGS, allocated multi-currency OPEX, and bank statements to produce a trustworthy monthly P&L.
* **[travel-agency-accounting-excel-template](https://github.com/HyVoid/travel-agency-accounting-excel-template)** — Which tour bookings actually generate net profit and positive cash flow after supplier costs and B2B collections? — Calculate per-booking tour job costs, gross margins, AR/AP settlement, and operating cash flow across multiple currencies.

## About Theseus Workshop

We build practical, audit-ready financial and operational Microsoft Excel models for wholesale, manufacturing, and operator-led businesses that need institutional treasury and accounting control inside standard spreadsheets.

Every workbook uses transparent native Excel formulas with zero black-box macros, giving finance and operations teams complete visibility into every weekly cash calculation.

Solving complex working capital, inventory procurement, or capital allocation problems in spreadsheets? **[Explore Our Full Collection of Financial & Operational Excel Templates at Theseus Workshop →](https://www.theseusworkshop.com)**

---

## License

Distributed under the [Apache License 2.0 Open Source License](https://www.apache.org/licenses/LICENSE-2.0).

