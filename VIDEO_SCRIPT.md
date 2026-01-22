# Demo Video Script (5–7 minutes)

## Goal
Show how the workbook converts an item catalog + assemblies into a clean estimate, and how the **Multiplier** enables quick scenario pricing.

---

## 0:00–0:20 — Intro
- “Hi, this is an Excel estimating mini-repo built as a portfolio demo.”
- “It shows item catalogs, assemblies, a robust builder, and an estimate rollup.”

## 0:20–1:10 — Repo structure
On screen: GitHub repo
- Point to `assets/Excel_Estimating_MiniRepo_Robust_EN.xlsx`
- Point to `docs/WALKTHROUGH.md`
- Mention: “No macros, no Power Query required. Designed to open cleanly in any locale.”

## 1:10–2:10 — Items_DB
Open workbook
- Show **Items_DB**
- Explain columns: Code, Category, Unit, Unit Cost
- Add one item live (optional) to show extensibility.

## 2:10–3:20 — Assemblies_DB
- Show **Assemblies_DB**
- Explain Assembly_Code, Seq, Key, Item_Code, Factor_Qty
- Highlight that `Key = Assembly_Code|01` makes it robust and predictable.

## 3:20–4:30 — Assembly Builder
- Go to **Assembly_Builder**
- Select `ASM-POOL-CORE`
- Set Multiplier to `1.00`
- Explain: Qty = Factor_Qty × Multiplier
- Switch multiplier to `1.25` and show how all quantities and totals scale.

## 4:30–6:00 — Estimate
- Go to **Estimate**
- Copy Item_Code + Qty from builder and paste into Estimate
- Show how Description/Unit/Unit_Cost populate automatically
- Show subtotal and pricing components (Overhead, Profit, Tax)
- Mention validation column (Missing Code / Missing Qty).

## 6:00–6:40 — Scenario comparison
- Scenario A: 1.00
- Scenario B: 1.25
- “This is how you generate option pricing quickly.”

## 6:40–7:00 — Wrap-up
- “This pattern generalizes to remodeling, civil works, and any scope with repeatable packages.”
- “Thanks—feel free to clone the repo and test with your own items and assemblies.”

---

## Recording tips
- Record at 1080p
- Zoom to 125% in Excel for readability
- Keep mouse movements slow
- Use a short on-screen checklist (Inputs → Builder → Estimate)
