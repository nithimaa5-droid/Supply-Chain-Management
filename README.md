# 🚚 Supply Chain Management Portfolio

**Electronics & Communication Engineer → Customer Success Associate → Supply Chain Analyst (Procurement · Inventory · SAP MM)**

I use an engineering mindset and data analysis to make procurement and inventory decisions measurable.

[LinkedIn](https://www.linkedin.com/in/nithya-shree-9b5978335/?isSelfProfile=true) · [Email](#) · [Resume](#) · [GitHub](#)

---

## 👋 Profile Summary

Electronics and Communication Engineering graduate focused on **procurement, inventory planning, and SAP MM**. I build small, complete projects that follow one pattern: **problem → data → method → findings → recommendation.**

**Open to:** Supply Chain Analyst · Procurement Executive · Inventory / Materials Planner · SAP MM Trainee roles

### Why Engineering → Supply Chain?

| Engineering strength | How it applies in supply chain |
|---|---|
| Systems thinking | Seeing the supply chain as connected stages (plan → source → make → deliver) and spotting where one stage causes problems in another |
| Signal vs. noise | Separating real demand patterns from random variation when setting safety stock |
| Troubleshooting | Tracing root causes of stockouts, late deliveries, or invoice mismatches step by step |
| Quantitative comfort | Working with formulas, statistics, and data tools without hesitation |

---

## 🧰 Skills & Tools

| Area | Skills | Level |
|---|---|---|
| **Procurement & Sourcing** | Supplier evaluation, RFQ comparison, total cost of ownership, purchase-to-pay | Working knowledge |
| **Inventory Management** | Safety stock, reorder point, EOQ, ABC/XYZ analysis, inventory turnover | Working knowledge |
| **Demand & Logistics** | Moving average, exponential smoothing, forecast accuracy (MAPE), warehousing basics | Learning |
| **ERP** | SAP MM: master data, purchasing, goods receipt, invoice verification | Learning |
| **Analytics** | Excel (pivot tables, XLOOKUP, charts, dashboards), SQL (joins, GROUP BY, aggregation) | Working knowledge |

---

## ⭐ Featured Project: Inventory Analysis

> **Status:** 🔄 In progress · **Tools:** Excel · **Folder:** [`/inventory-analysis`](./inventory-analysis)

**Business problem:** A company holds many SKUs. Some are overstocked and tie up cash, while others stock out and delay production or sales. Which items need attention first, and how much should be ordered and when?

**Approach**
1. Clean the dataset (item, annual demand, unit cost, lead time, current stock)
2. **ABC classification** by annual consumption value (A ≈ top 80% of value, B ≈ next 15%, C ≈ last 5%)
3. Calculate **safety stock** and **reorder point** per item
4. Calculate **EOQ** for A-class items
5. Flag items currently below reorder point

**Findings** *(fill in after completing the analysis)*
- `__%` of SKUs account for `__%` of consumption value
- `__` items are below their reorder point and at risk of stockout
- `__` C-class items appear overstocked, tying up about `₹__` in working capital

**Recommendations** *(fill in)*
- Tighter review cycle for A items, simpler min-max rules for C items
- Reorder quantities and timing for the highest-risk items

📸 *Add a screenshot of your Excel dashboard here.*

---

## 🗺️ Project Roadmap

| Project | What it demonstrates | Tools | Status |
|---|---|---|---|
| 📦 **Inventory Analysis** | ABC analysis, safety stock, reorder point, EOQ | Excel | 🔄 In progress |
| 🤝 **Supplier Scorecard** | Weighted supplier ranking on cost, quality, delivery | Excel | 📝 Planned |
| 💻 **SAP MM Procure-to-Pay Walkthrough** | PR → PO → GR → invoice verification, documented with screenshots | SAP MM | 📝 Planned |
| 🏭 **Manufacturing Material Flow** | Material flow from supplier to production line | Process maps | 📝 Planned |
| 📊 **Operations Analytics** | Root-cause analysis of late deliveries and stockouts | SQL, Excel | 📝 Planned |

Each project folder follows the same template: **problem statement → data → approach → analysis → findings → recommendations.**

---

## 📐 Core Concepts Quick Reference

| Concept | Formula | Meaning |
|---|---|---|
| **Safety Stock** | `Z × σd × √L` | Buffer against demand variability during lead time |
| **Reorder Point** | `(Avg daily demand × Lead time) + Safety stock` | Stock level that triggers a new order |
| **EOQ** | `√(2DS / H)` | Order quantity that minimizes ordering + holding cost |
| **Inventory Turnover** | `COGS / Average inventory` | How many times stock is sold and replaced per year |
| **Days of Inventory** | `365 / Inventory turnover` | How long stock sits before use |
| **Fill Rate** | `Units shipped on time / Units ordered` | Share of demand met from stock |
| **OTIF** | `Orders On Time and In Full / Total orders` | Delivery reliability |
| **MAPE** | `Avg(\|Actual − Forecast\| / Actual)` | Forecast error |

*Z-values: 90% → 1.28 · 95% → 1.65 · 99% → 2.33*
*(D = annual demand, S = cost per order, H = holding cost per unit per year, L = lead time, σd = std. deviation of daily demand)*

### Worked Example

**EOQ:** D = 12,000 units/yr, S = ₹500/order, H = ₹20/unit/yr
EOQ = √(2 × 12,000 × 500 / 20) = √600,000 ≈ **775 units**

**Reorder Point:** daily demand = 40, lead time = 5 days, σd = 8, 95% service level
Safety stock = 1.65 × 8 × √5 ≈ **30 units**
ROP = (40 × 5) + 30 = **230 units**

---

## 💻 SAP MM: Procure-to-Pay Flow

| Step | Business meaning | Typical T-code |
|---|---|---|
| 1. Purchase Requisition | Internal request for material or service | `ME51N` |
| 2. RFQ / Quotation | Request and compare supplier quotes | `ME41` / `ME47` / `ME49` |
| 3. Purchase Order | Formal order sent to supplier | `ME21N` |
| 4. Goods Receipt | Material received, stock updated | `MIGO` (movement type 101) |
| 5. Invoice Verification | Supplier invoice matched to PO and GR (three-way match) | `MIRO` |
| 6. Payment | Vendor paid by Finance | `F110` (FI) |

**Useful for review:** `MM01` (create material) · `ME23N` (display PO) · `MMBE` (stock overview) · `MB52` (warehouse stock) · `ME2M` (POs by material)

> T-codes can vary by system and version, so verify in your SAP training environment.

---

## 🎤 Interview Prep

<details>
<summary><b>Walk me through your portfolio.</b></summary>

I started with the fundamentals of procurement and inventory, then built projects around real decisions. In my inventory analysis I classified SKUs with ABC analysis, calculated safety stock and reorder points, and identified which items needed action first. Next I'm building a supplier scorecard and documenting the SAP MM purchase-to-pay flow.
</details>

<details>
<summary><b>Why supply chain after electronics engineering?</b></summary>

Supply chains are systems with inputs, constraints, variability, and feedback loops, which is how I was trained to think. I enjoy using data to find where a process breaks and what to change.
</details>

<details>
<summary><b>How do you decide how much safety stock to hold?</b></summary>

It depends on demand variability, lead time, and the service level the business wants. I use `Z × σd × √L`. Higher service levels cost more in holding cost, so the target should reflect the item's importance, which is why I pair it with ABC classification.
</details>

<details>
<summary><b>How would you evaluate and select a supplier?</b></summary>

I'd score suppliers on weighted criteria such as total cost, quality (defect rate), on-time delivery, lead time, and financial stability. Price alone is misleading, so I'd consider total cost of ownership. For critical items I'd also consider a backup source.
</details>

<details>
<summary><b>Explain three-way match.</b></summary>

Before paying, the system compares the purchase order (what was ordered), the goods receipt (what arrived), and the supplier invoice (what is being billed). Mismatches in quantity or price are blocked and investigated.
</details>

<details>
<summary><b>What would you do if a key supplier is late repeatedly?</b></summary>

Quantify the impact first (late deliveries, stockouts, cost). Then find the root cause with the supplier, agree on a corrective plan, and review performance with a scorecard. In parallel, raise safety stock for affected items and qualify an alternate supplier.
</details>

<details>
<summary><b>What is the difference between ABC and XYZ analysis?</b></summary>

ABC ranks items by value (how much money they represent). XYZ ranks items by demand variability (how predictable they are). Combining them shows, for example, that high-value, unpredictable items (AZ) need the closest attention.
</details>

---

## 📁 Repository Structure

```
├── inventory-analysis/        # ABC, safety stock, ROP, EOQ (Excel)
├── supplier-evaluation/       # weighted scorecard
├── sap-mm-workflows/          # P2P documentation + screenshots
├── manufacturing-supply-chain/
├── operations-analytics/      # SQL + Excel investigations
└── notes/                     # concept summaries and learning log
```

---

## 🎯 Goals

- Build end-to-end understanding of supply chain operations
- Gain project-backed skills in procurement and inventory planning
- Become proficient in SAP MM and enterprise purchasing processes
- Turn operational data into clear, actionable recommendations

## 🌱 Currently

Completing the inventory analysis project, then moving on to the supplier scorecard and the SAP MM walkthrough.

---

*Learning by doing. Improving through practice. One project at a time.* 🚀
