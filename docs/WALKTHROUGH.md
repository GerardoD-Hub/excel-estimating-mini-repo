# Walkthrough: How to Review This Mini-Repo

This repository is an Excel estimating workflow built for portfolio/demo purposes.

## 1) Open the workbook
Open:
- `assets/Excel_EstimMiniRepo_Robust_EN_LocaleSafe.xlsx`

If Excel prompts about external links/macros:
- Choose **Do not enable macros** (there are no macros)
- Choose **Update links = No** (there are no external links)

## 2) Inputs (pricing rules)
Go to **Inputs** and confirm:
- Overhead Method: Percent (or Weekly)
- Overhead %, Profit %, Tax %
- Duration (weeks) and Weekly Indirects (if using Weekly)

## 3) Generate an assembly
Go to **Assembly_Builder**:
- Pick `ASM-POOL-CORE` in **B3**
- Set **Multiplier** to `1.00`

You should see rows populate with:
- Item_Code, Factor_Qty, Qty, Unit_Cost, Line_Total

## 4) Build an estimate
Go to **Estimate**:
- Copy from the builder:
  - Item_Code (column B) → paste into Estimate column A
  - Qty (column D) → paste into Estimate column D
- The sheet auto-fills Description/Unit/Unit_Cost and calculates totals.

## 5) Compare scenarios (Base vs +25%)
Scenario A:
- Builder Multiplier = `1.00`

Scenario B:
- Builder Multiplier = `1.25`

Duplicate the workbook or paste Scenario B into a new section of Estimate to compare totals.

## 6) Review totals
At the bottom of **Estimate**, review:
- Subtotal (Direct Costs)
- Overhead
- Profit
- Tax
- Grand Total
