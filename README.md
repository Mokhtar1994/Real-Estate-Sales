# 🏢 Real Estate Sales & Collections Dashboard | Power BI (Graduation Project)

Graduation project for the **Route Data Analysis Diploma**: an enterprise-style Power BI report that tracks **unit sales, installment collections, and outstanding balances** across **8 real estate developments**, with separate views for **cash** and **bank-financed** buyers.
---

## 🎯 Objective

Give management a clear, single view of the sales and collection performance of every project:

- How many units are sold in each project, and what share of the advertised units does that represent?
- How much of the invoiced installment amount has actually been collected, and how much is still outstanding?
- Which installments (1 to 7) are paid, due but unpaid, or not yet due?
- How do **cash buyers** compare with **bank-financed buyers**, and which banks collect best?
- How does construction progress relate to collections?

---

## 🛠️ Tools & Skills

| Area | Details |
|---|---|
| **BI Tool** | Power BI Desktop |
| **Data Preparation** | Power Query (M): combined and unpivoted 8 Excel worksheets, parsed Arabic-format installment text (paid / not due / amount due) into numeric values and status |
| **Data Modeling** | Fact tables per project, summary tables (Global Summary, Collection by Date), and a `DimDate` table |
| **DAX** | Sold Count, Sold %, Collection Rate, Issued / Collected / Outstanding Invoices, Outstanding Balance and %, Project Completion %, cash vs. bank measures |
| **Report Design** | 34-page report, bookmark-based navigation (Home page to Global Summary to Project to Cash / Bank / Bank-wise views), pivot tables, combo charts, pie charts, KPI cards, slicers |

---

## 📂 Data

- **Sales data:** one Excel worksheet per project (8 worksheets), with unit price, payment plan, 7 installment columns, total due, total paid, bank, sale contract date, and construction completion %.
- **Advertised units:** a separate Excel file with the total advertised units for each project, used to calculate Sold %.
- **Data challenge:** installment columns mix text and numbers (`"تم السداد 660,600"` = paid, `"غير مستحقة"` = not due, a plain number = due but unpaid), so each cell was classified into one of three states before calculating collections.

> ⚠️ The original data files are **not included** in this repository because they contain customer information.

---

## 📊 Report Structure (34 pages)

| Section | Content |
|---|---|
| **Main Page** | Navigation hub to all projects and summary pages |
| **Global Summary** | All 8 projects side by side: units, sold %, invoiced, collected, outstanding (bank and cash) |
| **Collection by Date Summary** | Collected and outstanding amounts for new vs. old contracts, with a date slicer |
| **Per project (×8)** | **Overall**, **Cash**, **Bank**, and **Bank-wise** views: KPI cards (total units, price, sold %, completion %), installment-level charts for collected amount, outstanding amount, and outstanding invoices, and a collected vs. outstanding pie chart |

Projects: Degla Landmark · Crystal Plaza Maadi · One Kattameya · Skyline Katameya · Degla Palms 6 October · Lake Front 6 · Rihana · Zahra North Coast

---

## 💡 Key Insights

1. **Scale:** 3,088 units sold across 8 projects, worth **EGP 18.6B** in contract value. **EGP 13.1B (about 70%)** has been collected so far.
2. **Strong collection on due installments:** **94.3%** of invoiced (due) installment amounts were collected, leaving **EGP 0.79B** due but unpaid.
3. **Collection varies a lot by project:** Skyline Katameya (96.3%), Crystal Plaza (95.9%), One Kattameya (95.1%), and Degla Landmark (94.7%) perform best, while **Lake Front 6 is the weakest at 75.0%**, followed by Zahra North Coast (81.2%) and Degla Palms (86.3%). Lake Front 6 and Degla Palms also have the lowest construction progress.
4. **Banks finance most units, cash brings the most value:** about **78%** of units are bank-financed, but cash buyers account for about **35%** of total contract value (average unit price EGP 9.7M vs. EGP 5.0M for bank buyers), driven mostly by Skyline Katameya.
5. **Bank performance differs:** the biggest banks (National Bank of Egypt, Banque Misr, CIB) collect at about 94–95%, while smaller banks such as QNB Egypt are much lower (about 73%).
6. **Sales progress:** Rihana (51%) and Crystal Plaza (50%) have sold about half of their advertised units, while Skyline Katameya, Degla Palms, and Zahra North Coast have sold under 5%.
7. **Skyline Katameya** alone represents about **30%** of total contract value, with an average unit price of about EGP 10.7M, roughly double the other projects.
8. **Standardized payment plans:** about **53%** of contracts follow the same 7-installment plan (20%, 20%, 20%, 15%, 15%, 5%, 5%).

---

## 🧮 DAX Measures

Sold Count · Sold % · Total Units · Units Price · Amount Collected · Outstanding Balance · Outstanding % · Collection Rate · Issued Invoices · Collected Invoices · Outstanding Invoices · Project Completion %
---

## 📁 Repository Structure

```
real-estate-sales-dashboard/
├── README.md
├── home-page.png
├── global-summary.png
├── project-overview.png
├── cash-view.png
└── bank-view.png
```

The `.pbix` and Excel files are intentionally **not** uploaded (see the note above).

---

## 👤 Author

**Muhammed Mokhtar** — Data Analyst
📍 Alexandria, Egypt
🔗 [LinkedIn](https://linkedin.com/in/mohammed-mokhtar-3126a1167)
