# UP State Budget (2026-27) — Data Extraction & Analysis

A data science project that extracts, cleans, and analyzes structured financial data from a Hindi government budget PDF.

---

## 📌 Objective

Extracted structured financial data from **Pages 8–10** of the Uttar Pradesh State Budget 2026-27 (`khand2part2_2026_2027.pdf`) — a Hindi-language PDF. The pipeline handles OCR extraction, data cleaning (including structural column shifts and CID tag artifacts), and produces trend analysis across four financial periods (Actuals 24-25, Budget 25-26, Revised 25-26, Budget 26-27).

---

## 🛠 Tech Stack

| Tool | Purpose |
|------|---------|
| **Python** | Core language |
| **pdfplumber** | OCR extraction from PDF |
| **Pandas** | Data cleaning, manipulation, and analysis |
| **Matplotlib** | Charts and visualizations |
| **Regex** | Parsing OCR output and fixing Hindi text artifacts |
| **Jupyter Notebook** | Interactive analysis environment |
| **NumPy** | Numerical support |

---

## ⚙️ Installation

Clone the repository and install the required dependencies:

```bash
pip install pandas pdfplumber matplotlib jupyter numpy
```

Then launch the notebook:

```bash
jupyter notebook "CEGIS_Assessment(Aryan_Chauhan).ipynb"
```

---

## 💡 Key Insights

| # | Finding |
|---|---------|
| 1 | **~51% budget growth** — Total expenditure grew from ₹62,061 Cr (Actuals 24-25) to ₹94,003 Cr (Budget 26-27) over 2 years. |
| 2 | **Revenue dominates (~70%)** — Reflects a service-heavy, transfer-oriented expenditure profile (salaries, pensions, grants). |
| 3 | **Major Construction Works (#24)** is the single largest capital expenditure head, rising to ₹11,263 Cr in Budget 26-27. |
| 4 | **Office Expenditure (#8)** recorded the highest % growth — up **136.7%** in Budget 26-27 vs Budget 25-26. |
| 5 | Several large transfer heads (subsidies, grants, social security) show **Revised < Budget**, indicating under-utilisation in 2025-26. |

---

## 📂 Project Structure

```
├── CEGIS_Assessment(Aryan_Chauhan).ipynb   # Main Jupyter notebook
├── khand2part2_2026_2027.pdf               # Source: UP Budget PDF (Hindi)
├── UP_Budget.csv                           # Raw OCR extraction output
├── UP_Budget(Updated).csv                  # Cleaned intermediate dataset
├── UP_Budget_Corrected.csv                 # Final corrected dataset (used for analysis)
└── README.md                               # This file
```

---

## 🗂 Pipeline Overview

```
PDF (Hindi, Pages 8–10)
        │
        ▼
  OCR Extraction (pdfplumber + Relaxed Regex)
        │
        ▼
  Data Cleaning
  • Remove garbage header rows
  • Remove grand-total duplicate rows
  • Fix Hindi text OCR artifacts
  • Correct structural column shift (Item 24)
        │
        ▼
  Analysis & Visualisation
  • Revenue vs Capital composition
  • Year-on-Year grand total trend
  • Top expenditure heads
  • Utilisation rate (Budget vs Revised)
  • Biggest gainers / losers (Budget 26-27 vs Budget 25-26)
```

---

## 📊 How to View

### Option 1 — Jupyter Notebook (Full Code + Outputs)
Run `jupyter notebook` in this directory and open `CEGIS_Assessment(Aryan_Chauhan).ipynb`.

### Option 2 — GitHub Notebook Viewer
GitHub renders `.ipynb` files natively — scroll through the notebook directly on this page to see all code cells and chart outputs without any installation.

---

## 📋 Data Source

**Source:** Uttar Pradesh State Budget 2026-27 — *Khand 2, Part 2*  
**Tables Extracted:** Pages 8–10 — Standard Object-wise Statement of Expenditure (Gross), ₹ in Lakhs  
**Language:** Hindi (Devanagari script)

---

*Submitted as part of the CEGIS Data Science Assessment.*
