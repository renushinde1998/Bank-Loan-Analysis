Bank Loan Analysis Report - Power BI Project
Overview
This project involves analyzing bank loan data to derive insights regarding loan performance, funding trends, interest rates, and borrower profiles. The project utilizes Power BI for visualization, with data processing and analysis carried out using DAX (Data Analysis Expressions) for calculated measures and custom queries.

Table of Contents
Project Description
Features
Technologies Used
Data Source
Data Preparation
DAX Queries and Measures
Key Visuals
How to Use
Future Enhancements
Project Description
The Bank Loan Analysis Report is designed to provide stakeholders with insights into loan performance. The report helps to track key metrics such as funded amounts, received amounts, average interest rates, and loan performance across different categories, including loan status, purpose, and borrower attributes.

Features
Data Cleaning: The raw dataset was cleaned to address missing data, duplicates, and format inconsistencies.
Data Modeling: Relationships were established between various tables for efficient querying and visualization.
DAX Queries & Measures: Custom DAX queries were used to calculate key metrics like:
Total Funded Amount
Total Received Amount
Average Interest Rate
Loan performance indicators
Time Intelligence: MTD (Month-to-Date) and MoM (Month-over-Month) measures were created for dynamic time-based analysis.
Interactive Dashboards: The report features interactive visuals that allow users to filter by loan status, loan purpose, grade, home ownership, and more.
Technologies Used
Power BI: For creating dashboards and visuals.
DAX (Data Analysis Expressions): For writing custom measures and queries.
SQL: For querying and transforming data before loading into Power BI.
Data Modeling: Power BI’s data modeling capabilities to manage relationships between multiple tables.
Data Source
The dataset contains information on loan applications, including the funded amount, received amount, interest rates, and loan statuses such as charged off, fully paid, or current. Data includes borrower details like home ownership, loan grade, and purpose of loans.

Data Preparation
Data Cleaning: Removed duplicates, handled missing values, standardized data formats.
Transformation: Converted raw data into a format that is compatible with Power BI, optimizing it for analysis.
Data Modeling: Defined relationships between multiple tables (loan applications, borrower details, loan statuses) to streamline data queries.
DAX Queries and Measures
Key DAX measures created in the project:

Total Funded Amount: CALCULATE(SUM('LoanData'[Funded Amount]))
Average Interest Rate: AVERAGE('LoanData'[Interest Rate])
MTD Funded Amount: TOTALMTD(SUM('LoanData'[Funded Amount]), 'LoanData'[Date])
Loan Performance (Good vs. Bad Loans): SWITCH(TRUE(), 'LoanData'[Loan Status] = "Fully Paid", "Good Loan", "Bad Loan")
Additional DAX queries include calculations for MoM growth rates and metrics for each loan status category.

Key Visuals
Loan Performance Breakdown:

Good vs. Bad loans based on loan status (Fully Paid, Charged Off, Current).
Visualized via pie charts and bar graphs.
Funded Amount by Purpose:

Comparison of funded amounts for different loan purposes such as debt consolidation, credit card, home improvement.
Visualized using bar charts.
Loan Distribution by Term:

Analysis of loans by term length (36 months, 60 months).
Visualized using stacked column charts.
Loan Trends by State:

Heatmap to visualize loan distribution across different states.
How to Use
Clone the repository:
bash
Copy code
git clone https://github.com/your-username/bank-loan-analysis-report.git
Open the Power BI report file Bank_Loan_Report.pbix in Power BI Desktop.
Refresh the data to ensure the latest information is loaded.
Interact with the visuals by selecting filters (loan status, loan purpose, grade, etc.) to drill into specific data points.
Future Enhancements
Add more advanced DAX measures for predicting loan defaults.
Incorporate external datasets (e.g., economic indicators) to enrich analysis.
Develop forecasting models using Power BI’s AI capabilities.
Improve interactivity with more drill-down capabilities.
