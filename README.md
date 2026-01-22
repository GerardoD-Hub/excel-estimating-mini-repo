## Quick links
> Locale note: Excel displays formulas in your language automatically (e.g., VLOOKUP shows as BUSCARV in Spanish). The LocaleSafe file is included to avoid any regional issues.

- **Download workbook (recommended, locale-safe):** `assets/Excel_EstimMiniRepo_Robust_EN_LocaleSafe.xlsx`
- **Download workbook (original):** `assets/Excel_EstimMiniRepo_Robust_EN.xlsx`
- **2-minute walkthrough:** `docs/WALKTHROUGH.md`
- **Demo video script:** `docs/VIDEO_SCRIPT.md`
# Excel Estimating Mini-Repo (Robust Assemblies)
- **Download workbook:** `assets/Excel_Estimating_MiniRepo_Robust_EN.xlsx`  
- **2-minute walkthrough:** `docs/WALKTHROUGH.md`  
- **Demo video script:** `docs/VIDEO_SCRIPT.md`

A small, portfolio-friendly Excel estimating workflow that demonstrates:

- **Item database** (Items_DB) with standardized codes, units, and unit costs  
- **Assemblies** (Assemblies_DB) to package repeated scopes (e.g., pool core, finishes, landscaping)  
- A **robust Assembly Builder** that scales quantities using a single **Multiplier** (no dynamic arrays, no AGGREGATE)  
- An **Estimate** sheet that rolls up **Direct Costs + Overhead + Profit + Tax**

> Designed to open cleanly in **any Excel locale**. Excel stores formulas internally in English; your local Excel will display them translated.

---

## Quick start (2 minutes)

1. Open: `assets/Excel_Estimating_MiniRepo_Robust_EN.xlsx`
2. Go to **Inputs**  
   - Set **Overhead Method** (Percent or Weekly)  
   - Adjust **Overhead %, Profit %, Tax %, Duration**
3. Go to **Assembly_Builder**  
   - Pick an **Assembly Code** (cell **B3**)  
   - Set **Multiplier** (cell **B4**)  
   - Review generated items (Item_Code, Qty, Line_Total)
4. Copy **Item_Code** + **Qty** and paste into **Estimate** (columns A and D)
5. Review totals at the bottom of **Estimate**

---

## What “Multiplier” means

For every assembly line:

**Qty = Factor_Qty × Multiplier**

Examples:
- `1.00` = base package  
- `1.25` = +25% scope (bigger pool/deck, more lights/landscape)  
- `0.80` = -20% scope  

---

## Sheet guide

- **Inputs**: project parameters and pricing rules (Overhead, Profit, Tax)
- **Items_DB**: master item catalog (Code, Unit, Unit Cost)
- **Assemblies_DB**: assembly recipes. Each item has:
  - `Seq` (1..n) and a stable `Key` = `Assembly_Code|01`
- **Assembly_Builder**: robust generator (VLOOKUP by Key)
- **Estimate**: estimating worksheet + rollup totals
- **Instructions**: short notes and reminders

---

## Assemblies included (examples)

- `ASM-POOL-CORE` — Pool core package
- `ASM-POOL-FIN` — Pool finishes package
- `ASM-LAND` — Landscaping package
- `ASM-LIGHT` — Exterior + pool lighting package
- `ASM-EQUIP` — Pool equipment package

---

## Units cheat sheet

- **LS** lump sum  
- **EA** each  
- **LF / LM** linear foot / linear meter  
- **SF / m²** square foot / square meter  
- **CY / m³** cubic yard / cubic meter  
- **LB / TON** pound / ton  
- **HR / DAY / WK** hour / day / week  
- **GAL / L** gallon / liter  
- **SET** kit/set

---

## Suggested demo video (5–7 minutes)

See: `docs/VIDEO_SCRIPT.md`

---

## License

MIT — see `LICENSE`.
