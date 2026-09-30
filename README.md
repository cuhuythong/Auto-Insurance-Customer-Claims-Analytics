# Auto Insurance Customer & Claims Analytics

Interactive **Tableau business analytics** project using **10,000 auto-insurance records** to explore customer value, policy and vehicle characteristics, premiums, and claim behavior. The project combines data preparation, KPI development, exploratory analysis, interactive dashboards, and data storytelling to support customer segmentation, pricing, underwriting, and risk-management decisions.

![Auto Insurance Dashboard project cover](images/project_cover.png)

> **Tools:** Tableau · Data Visualization · EDA · KPI Development · Business Analytics · Data Storytelling  
> **Dataset:** 10,000 records · 24 original variables  
> **Deliverable:** Packaged Tableau workbook (`.twbx`) with interactive dashboards, parameters, filters, calculated fields, and a Tableau Story

## Business Problem

The project frames the analysis around **PrimeShield Insurance**, a fictional auto insurer facing profitability pressure from rising claim costs, uneven customer risk, and pricing inefficiencies. The goal is to identify meaningful customer, policy, vehicle, and claim patterns that can support better segmentation and business decisions.

The analysis was developed for **OPIM 5605: Data Visualization and Communication** at the University of Connecticut as a four-person team project.

## Business Questions

The analysis addresses questions such as:

- Which customer demographics are associated with higher Customer Lifetime Value (CLV)?
- How does income relate to policy type and coverage selection?
- Which sales channels attract higher-value customers?
- How do premiums vary across customer and vehicle segments?
- Which customer or vehicle characteristics are associated with higher claim amounts?
- How do policy type and coverage relate to claim magnitude or frequency?
- How do income and CLV tiers relate to claim behavior?

## Dataset & Preparation

The raw dataset contains **10,000 rows and 24 columns** covering demographics, policies, sales channels, vehicle characteristics, premiums, complaints, and claims. Representative fields include `State`, `Customer Lifetime Value`, `Coverage`, `Education`, `EmploymentStatus`, `Income`, `Monthly Premium Auto`, `Policy Type`, `Sales Channel`, `Total Claim Amount`, `Vehicle Class`, and `Vehicle Size`.

The repository includes both the supplied raw and cleaned datasets so the analysis inputs are transparent:

- `data/raw/auto_insurance_raw.csv` — original dataset used by the team.
- `data/processed/auto_insurance_cleaned.csv` — prepared version used for analysis; it removes the unique `Customer` identifier, standardizes the effective-date representation, and includes `Claim_to_Premium_Ratio`.

Dataset source referenced in the original project: Kaggle, **Auto Insurance Dataset** by `singhnproud77`.

## KPIs & Calculated Fields

| Metric | Tableau definition | Analytical purpose |
|---|---|---|
| **Claim Amount Min Threshold** | User-controlled parameter | Focus analysis on claims above a selected amount |
| **Claim to Income** | `Total Claim Amount / Income` | Compare claim burden relative to customer income |
| **Premium Efficiency** | `Total Claim Amount / Monthly Premium Auto` | Compare claim payouts with monthly premium |
| **Claim Frequency** | `Months Since Policy Inception / (Months Since Last Claim + 1)` | Examine claim activity relative to policy tenure |
| **Income Tier** | Low / Medium / High | Segment customers by income |
| **CLV Tier** | Low / Medium / High | Segment customers by customer lifetime value |

The Tableau workbook also contains parameters that dynamically switch among demographic, policy, and vehicle dimensions, allowing the same views to support multiple analytical questions.

## Interactive Tableau Analysis

The packaged workbook contains **14 worksheets** and four primary presentation views:

### Customer Dashboard
Explores customer segmentation, geographic distribution, sales channels, policy and coverage selection, income, CLV, and demographic patterns.

### Claim Dashboard
Examines claim behavior across demographics, employment and education groups, income and CLV segments, policy characteristics, coverage, and vehicle attributes.

### Introduction
Provides the project context and navigation into the analysis.

### Tableau Story
Connects the dashboards and analytical findings into a guided data-storytelling sequence.

The workbook is included at:

```text
tableau/auto_insurance_customer_claims_analytics.twbx
```

GitHub cannot render an interactive `.twbx` workbook directly. Download the workbook and open it in **Tableau Desktop** or a compatible Tableau application to use the filters, parameters, dashboards, and story.

## Selected Findings

The team's dashboard analysis identified several descriptive patterns in this dataset:

- Customers were most concentrated in California, while Washington had the fewest customers.
- Agents were the most common customer onboarding channel.
- Personal Auto was the most common policy type.
- Large luxury cars and luxury SUVs showed comparatively high claim amounts.
- Premium coverage showed higher average claim amounts in the dashboard analysis.
- Income, CLV, employment, vehicle characteristics, and policy features provided useful segmentation dimensions for examining customer value and claim behavior.

These findings describe patterns in this dataset and should not be interpreted as causal relationships.

## Business Recommendations

Based on the dashboard findings, the team proposed using customer and risk segmentation to inform pricing and underwriting, reviewing higher-risk customer and vehicle segments, strengthening agent-led acquisition while improving other sales channels, monitoring claim-heavy segments, and tailoring customer engagement to value and risk characteristics.

## Repository Structure

```text
auto-insurance-customer-claims-analytics/
├── README.md
├── .gitignore
├── data/
│   ├── raw/
│   │   └── auto_insurance_raw.csv
│   └── processed/
│       └── auto_insurance_cleaned.csv
├── tableau/
│   └── auto_insurance_customer_claims_analytics.twbx
└── images/
    └── project_cover.png
```

## How to Explore the Project

1. Clone or download the repository.
2. Open `tableau/auto_insurance_customer_claims_analytics.twbx` in Tableau Desktop or a compatible Tableau application.
3. Navigate through the **Customer Dashboard**, **Claim Dashboard**, and **The Story**.
4. Use the workbook's filters and parameters to explore customer and claim segments.
5. Review the raw and processed CSV files under `data/` to inspect the source and prepared data.

Because the `.twbx` is a packaged Tableau workbook, it contains the workbook resources and data connections needed for the project. The separate CSV files are included to make the raw-to-processed data organization visible outside Tableau.

## Skills Demonstrated

**Tableau · Interactive Dashboard Design · Data Visualization · Exploratory Data Analysis · Data Cleaning · Calculated Fields · Parameters · Filters · KPI Development · Business Analysis · Data Storytelling**

## Contributors

This project was completed collaboratively by:

- Allen Paul
- Shivani Murukannaiah
- **Thong Cu**
- Yeongeun Ra

## Portfolio Note

This repository presents the analytical deliverables of an academic team project in a concise portfolio format. The course syllabus and written project paper are intentionally excluded; the Tableau workbook, datasets, and README preserve the project work most relevant to reviewing the analysis.
