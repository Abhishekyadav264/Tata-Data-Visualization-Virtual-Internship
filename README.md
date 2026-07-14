# 📊 Tata Data Visualization Virtual Internship

![Tableau](https://img.shields.io/badge/Tableau-Visualization-E97627?logo=tableau)
![PowerBI](https://img.shields.io/badge/PowerBI-Alternative%20Tool-yellow?logo=powerbi)
![Excel](https://img.shields.io/badge/Excel-Raw%20Data-217346?logo=microsoftexcel)
![Status](https://img.shields.io/badge/Internship-Completed-brightgreen)

Completed coursework and deliverables for the **Tata Data Visualization: Empowering Business with Effective Insights** virtual experience programme (offered by Tata iQ / Tata Insights and Quants), covering business-question framing, chart selection, hands-on visual creation in Tableau, and a final stakeholder presentation.

---

## 🚀 Programme Overview

This repository documents my completion of Tata's **Data Visualization virtual experience programme**, delivered via Forage. The programme simulates the kind of real business problems that Tata Insights and Quants (Tata iQ) — a multidisciplinary data and analytics consultancy — solves for clients every day, using visualization tools like **Tableau** and **Power BI** to uncover insights buried in raw business data.

The programme is structured into **4 progressive modules**, each building on the last:

| Module | Focus |
|---|---|
| **1. Framing the Business Scenario** | Learning to anticipate the questions business leaders need answered |
| **2. Choosing the Right Visuals** | Matching the correct chart type to a given business scenario |
| **3. Creating Effective Visuals** | Cleaning data and building real visuals in Tableau/Power BI |
| **4. Communicating Insights and Analysis** | Presenting findings back to business leadership |

---

## 🎯 Business Scenario

An **online retail store** has hired me (in the role of a data consultant) to review its sales data and generate insights valuable to the **CEO** and **CMO**. The business has been performing well, and leadership wants to:

- Understand the major factors contributing to revenue, to plan strategically for next year.
- View performance metrics from both an **operations** and a **marketing** perspective.
- Identify which areas of the business are performing well, to support an **expansion strategy**.
- Break down metrics using the available customer demographic and country-level data.

A meeting with the CEO and CMO was framed as the goal throughout — every task in this repository builds toward that meeting.

---

## 📂 Project Structure

```
Tata-Data-Visualization-Virtual-Internship/
│
├── Task 1/
│   ├── Task1.pdf                          # Written CEO & CMO questions with justifications
│   └── Online Retail Data Set.xlsx        # Raw source dataset (541,909 transactions)
│
├── Task 2/
│   └── quiz.docx                          # Completed chart-selection quiz (5 questions)
│
├── Task 3/
│   └── Task3.twb                          # Tableau workbook with 4 visuals (Question1–Question4 tabs)
│
├── Task 4.mp4                             # Recorded stakeholder presentation video (~5 minutes)
│
└── README.md
```

---

## 🗂️ Dataset Description

The dataset used throughout the programme is the classic **"Online Retail" transactional dataset** (`Online Retail Data Set.xlsx`), containing **541,909 transaction records** from a UK-based online retailer, spanning the year 2010–2011.

| Column | Description |
|---|---|
| `InvoiceNo` | Unique invoice/transaction number |
| `StockCode` | Product/item code |
| `Description` | Product name |
| `Quantity` | Number of units purchased (contains some negative values — returns) |
| `InvoiceDate` | Date and time of the transaction |
| `UnitPrice` | Price per unit (contains some erroneous zero/negative entries) |
| `CustomerID` | Unique customer identifier |
| `Country` | Country the order was shipped to |

This is real, "messy" transactional retail data — it includes return transactions (negative quantities) and data-entry errors (invalid unit prices), which is exactly what makes Task 3's data-cleaning step necessary.

---

## 📝 Task 1 — Framing the Business Scenario

**Goal:** Learn how to anticipate the questions business leaders need answered, before building any visuals.

**Deliverable:** Draft 4 questions for the CEO and 4 questions for the CMO (8 total), thinking both quantitatively and qualitatively, reflecting how each leader views the business differently.

### Questions drafted for the CEO (operations/revenue lens):
1. **Which region is generating the highest revenue, and which is generating the lowest?** — to identify where to double down and where to investigate underperformance.
2. **What is the monthly trend of revenue — which months saw the biggest increase/decrease?** — to connect internal changes (launches, delays) to revenue swings.
3. **Which months generated the most revenue — is there seasonality in sales?** — to plan around predictable seasonal demand.
4. **Who are the top customers, and how much do they contribute to total revenue? Is the business dependent on them, or is the customer base diversified?** — to flag concentration risk vs. a healthy, diversified customer base.

### Questions drafted for the CMO (customer/marketing lens):
1. **What percentage of customers are repeat orders, and are they buying the same or different products?** — to gauge loyalty and inform re-targeting strategy.
2. **For repeat customers, how long between orders?** — to understand purchase cadence and time marketing touchpoints effectively.
3. **How much revenue comes from customers who've ordered more than once?** — to quantify the value of retention vs. acquisition.
4. **Who are the most frequent repeat customers, and how much do they contribute to revenue?** — to distinguish high-frequency/low-value customers (who may need bulk discounts) from high-value/low-frequency customers (who need consistent stock availability).

*(Full write-up with detailed justifications for each question is available in `Task 1/Task1.pdf`.)*

---

## 🎨 Task 2 — Choosing the Right Visuals

**Goal:** Practice matching the correct chart type to a specific business visualization request — since the wrong chart can lead to the wrong message or a bad decision by leadership.

**Format:** 5-question multiple-choice quiz, each posing a CEO/CMO visualization request.

| # | Scenario | Chart Selected |
|---|---|---|
| 1 | CEO wants a full-year revenue time series to spot seasonal trends | **Line Chart** |
| 2 | CMO wants top 10 countries by revenue, broken down further by product | **Stacked Bar Chart** |
| 3 | CEO wants min, Q1, median, Q3, and max of average revenue per country in one view | **Box Plot** |
| 4 | CMO wants top 10 customers by revenue, sorted highest to lowest | **Column Chart** |
| 5 | CEO wants demand by region across all countries, viewable at a glance with no scrolling/hovering | **Map Chart** |

*(Full quiz responses are in `Task 2/quiz.docx`.)*

---

## 📈 Task 3 — Creating Effective Visuals

**Goal:** Clean the raw dataset and build the actual visuals requested by the CEO/CMO in Tableau.

### Data Cleaning Steps Applied
Before any visual was built, the raw dataset was cleaned to remove bad data using conditional filters:
- **Removed rows where `Quantity < 1`** — filtering out returns (negative quantities) and zero-quantity entries.
- **Removed rows where `UnitPrice < 0`** — filtering out erroneous/invalid price entries.

### Visuals Built (Tableau, `Task3.twb`)
Each visual was created on its own worksheet tab, named by question number (`Question1`–`Question4`):

| Tab | Business Question | What It Shows |
|---|---|---|
| **Question1** | CEO wants a month-by-month time series of 2011 revenue to spot seasonal trends and plan next year's forecast | Monthly revenue line/trend chart for 2011 |
| **Question2** | CMO wants the top 10 countries by revenue (excluding the UK), along with quantity sold | Top 10 non-UK countries — revenue and quantity |
| **Question3** | CMO wants the top 10 customers by revenue, ordered from highest to lowest | Descending column/bar chart of top 10 customers |
| **Question4** | CEO wants product demand across all countries (excluding the UK) in a single, scannable view for expansion planning | Map-based view of demand by country |

Excluding the UK in Questions 2 and 4 was a deliberate requirement from the CEO/CMO — since the UK is the home market and already dominant, removing it surfaces the **best international expansion opportunities**, which was the actual business goal behind the analysis.

---

## 🎤 Task 4 — Communicating Insights and Analysis

**Goal:** Present the Task 3 findings back to the CEO and CMO in a clear, business-focused way — not just a walkthrough of the charts, but the reasoning and recommendations behind them.

**Deliverable:** A ~5-minute recorded video presentation (`Task 4.mp4`) covering:
- The initial data load and clean-up process (to demonstrate due diligence and data integrity).
- A walkthrough of all four visuals from Task 3, explained in the context of the CEO's and CMO's original questions.
- Insights and recommendations tied directly to the business goal of **identifying the most lucrative expansion opportunities**.

---

## 💡 Key Takeaways

- Framing the *right business questions first* is more important than jumping straight into visuals — Task 1 forced thinking from the CEO's and CMO's distinct perspectives before touching any data.
- Chart choice is not cosmetic — a **line chart** for trends, a **stacked bar** for category breakdowns, a **box plot** for distribution summaries, a **column chart** for ranked comparisons, and a **map** for geographic demand each serve a specific communication purpose, and picking the wrong one actively misleads stakeholders.
- Real business data is messy — returns (negative quantities) and data-entry errors (invalid prices) must be explicitly filtered out before any analysis is trustworthy.
- Excluding the "home market" (UK) from country-level comparisons was necessary to make the analysis actually useful for the stated goal: finding new international growth opportunities, not just confirming the UK is the biggest market.
- Communicating insights to leadership requires narrating the *process* (data cleaning, methodology) as well as the *findings* — this builds trust in the analysis, not just the conclusion.

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Excel** | Reviewing and exploring the raw transactional dataset |
| **Tableau** | Data cleaning (conditional filters) and building all four visuals |
| *(Power BI was an accepted alternative for Task 3, per programme instructions)* | |

---

## 👀 How to View This Project

1. Read `Task 1/Task1.pdf` for the full CEO/CMO business-question framing exercise.
2. Read `Task 2/quiz.docx` for the chart-selection reasoning.
3. Open `Task 3/Task3.twb` in **Tableau Desktop** (free trial available) to explore the four interactive visuals (`Question1`–`Question4` tabs), built on the cleaned version of `Task 1/Online Retail Data Set.xlsx`.
4. Watch `Task 4.mp4` for the full stakeholder presentation walking through the data cleaning process and all four visuals with business commentary.

---

## 🎯 Skills Demonstrated

- **Business analysis:** translating a vague leadership ask ("help us understand performance") into specific, answerable, role-appropriate questions.
- **Data visualization theory:** matching chart type to data structure and communication intent (trend vs. ranking vs. distribution vs. geography).
- **Data cleaning:** applying conditional-filter logic to remove returns and invalid entries before analysis.
- **Tableau:** building multiple linked worksheets/visuals from a single cleaned data source.
- **Business communication:** presenting a full analytical narrative (data → cleaning → visuals → insights → recommendation) to a simulated executive audience.

---

## 📌 Conclusion

This project reflects a full, structured walk-through of the data visualization consulting process as practiced at Tata Insights and Quants — starting from understanding what business leaders actually need to know, through selecting and building the right visuals on real (messy) retail transaction data, and ending with a clear, narrated presentation of findings tied to a concrete business goal: identifying the best opportunities for international expansion.

---

## 👤 Author

**Abhishek**
Aspiring Data Analyst
