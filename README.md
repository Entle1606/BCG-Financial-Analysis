BCG Financial Analysis | SEC EDGAR (2023–2025)
A Python and Pandas financial analysis project examining Microsoft, Tesla, and Apple using financial figures from their annual SEC Form 10-K filings for fiscal years 2023–2025. The analysis compares revenue, profitability, balance-sheet position, and operating cash flow, with the goal of identifying insights that could support an AI-powered financial chatbot.
Project objectives
- Organize financial statement data into a reusable CSV dataset.
- Calculate year-over-year changes for key financial metrics.
- Compare financial performance across three companies and fiscal years.
- Visualize trends and summarize business-relevant findings.
- Explore how structured financial data can support question answering in a financial chatbot.
Dataset
The dataset contains nine company-year records and five core metrics, all expressed in USD millions:
Metric	Financial statement
Total Revenue	Consolidated Statements of Income / Operations
Net Income	Consolidated Statements of Income / Operations
Total Assets	Consolidated Balance Sheets
Total Liabilities	Consolidated Balance Sheets
Operating Cash Flow	Consolidated Statements of Cash Flows


Fiscal-year note: Microsoft and Apple do not use calendar-year reporting periods. The Year column identifies each company's fiscal year, so cross-company comparisons do not always cover identical dates.
Project structure
BCG-Financial-Analysis/
├── Financial_analysis.ipynb
├── data/
│   └── sec_financials_2023_2025.csv
└── README.md
Tools
- Python 3
- Pandas for data cleaning, grouping, and financial calculations
- Matplotlib for visualizations
- Jupyter Notebook for reproducible analysis and written interpretation
Getting started
1. Clone or download this repository.
2. Open the BCG-Financial-Analysis directory in VS Code or Jupyter.
3. Install the dependencies:
   python -m pip install pandas matplotlib notebook
4. Open Financial_analysis.ipynb and select a Python kernel.
5. Run all cells. The notebook loads the CSV from data/ using a relative project path.
Analysis workflow
1. Load and validate: Read the CSV, inspect the dataset, and check that all nine company-year records are present.
2. Calculate growth: Use Pandas groupby('Company').pct_change() to calculate year-over-year percentage changes in each financial metric.
3. Calculate ratios: Derive net profit margin and liabilities-to-assets percentage.
4. Compare: Review 2025 financial metrics and company-level changes from 2023 to 2025.
5. Visualize: Plot revenue, net income, operating cash flow, and profit margin trends.
6. Interpret: Document findings and potential financial chatbot applications.
Selected findings
Based on the working dataset:
- Microsoft: Revenue increased approximately 32.9% and net income 40.7% between FY2023 and FY2025.
- Tesla: Revenue declined approximately 2.0% while net income declined approximately 74.3% over the same fiscal-year labels.
- Apple: Revenue increased approximately 8.6% and net income 15.5%.
These comparisons show why a financial assistant should distinguish revenue growth from profitability, cash generation, and changes in the balance sheet.
Relevance to an AI-powered financial chatbot
The structured dataset could support queries such as:
- Which company had the strongest revenue growth between 2023 and 2025?
- How did Tesla's net income change over the period?
- Which company had the highest net profit margin in 2025?
- How did operating cash flow compare with net income?
Scope: This repository is a financial analysis notebook, not a deployed chatbot. A chatbot would require an additional question-answering interface and safeguards for source attribution and numerical accuracy.
Sources and limitations
Official SEC EDGAR company filing pages:
- Microsoft — CIK 789019
- Tesla — CIK 1318605
- Apple — CIK 320193
