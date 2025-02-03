# Hiring Task - ML: Marketing Insights for iGnosis Tech

Thank you for your interest in ML roles at iGnosis Tech. This repository contains a data analysis project developed to help our (hypothetical) marketing department identify the most profitable customers and the bestselling products. The goal is to focus marketing efforts on the right customer segments—such as married vs. unmarried, working vs. retired, and premium vs. budget buyers—and to highlight which products drive the most profit.

## Table of Contents

- [Overview](#overview)
- [Data Description](#data-description)
- [Methodology](#methodology)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Findings and Hypothesis](#findings-and-hypothesis)
- [License](#license)

## Overview

The marketing team needs insights on:
- **Top 3 Most Profitable Products:** Identify the products with the highest total sales.
- **Characteristics of Loyal Customers:** Determine the demographics (e.g., life stage, premium customer status) of the top 10% most loyal customers, based on transaction frequency.
- **Customer Preference Hypothesis:** Offer a hypothesis on why loyal customers prefer certain products.

These insights will help the marketing department position products better and target the most valuable customer segments.

## Data Description

Two datasets were used in this analysis:
- **purchase_behaviour.csv:** Contains demographic and behavioral data of loyalty card holders.
- **transaction_data.csv:** Contains transaction records, including product names, total sales, transaction dates, and loyalty card numbers.

> **Note:** The data can be downloaded from [this Google Drive folder](https://drive.google.com/drive/folders/1JLHEIQp95b6Jo3iiXGYfIdKUrs8uWJn1?usp=sharing).

## Methodology

1. **Data Cleaning and Preparation:**
   - Converted transaction dates to datetime format.
   - Cleaned product names by removing extraneous weight details.
   - Merged transaction data with purchase behavior using the loyalty card number.

2. **Analysis:**
   - **Profitability:** Calculated total sales per product and identified the top 3 most profitable products.
   - **Loyalty:** Computed loyalty metrics (transaction count and total spending) per customer. The top 10% of customers (by transaction frequency) were considered the most loyal.
   - **Customer Characteristics:** Merged loyalty metrics with demographic data to analyze life stage and premium customer distribution.
   - **Hypothesis:** Identified the top products preferred by loyal customers and proposed a hypothesis for their preference based on brand loyalty, consumption patterns, price sensitivity, and product availability.

3. **Visualization and Reporting:**
   - Generated plots to visualize the top products, life stage distribution, premium customer distribution, and preferred products among loyal customers.
   - Created a textual report summarizing the key findings and hypothesis.

## Project Structure

```
Marketing-Insights/
├── purchase_behaviour.csv         # Customer demographic and behavior data
├── transaction_data.csv           # Transaction records
├── marketing_insights.png         # Generated visualization of insights
├── marketing_report.txt           # Generated report summarizing findings
├── untitled19.ipynb               # Jupyter Notebook with the full analysis code              
└── README.md                      # This file
```

## Usage

### Prerequisites

- Python (>=3.7)
- Required Python packages:
  - `pandas`
  - `matplotlib`

Install the required packages using pip:

```bash
pip install pandas matplotlib
```

### Running the Analysis

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Rafe2001/TopProducts-and-CustomerInsights.git
   cd TopProducts-and-CustomerInsights
   ```

2. **Run the Jupyter Notebook:**

   Launch Jupyter Notebook and open `untitled19.ipynb`:

   
3. **Outputs:**
   - The generated visualizations will be saved as `outputs/marketing_insights.png`.
   - The marketing report summarizing your findings is saved as `outputs/marketing_report.txt`.

## Findings and Hypothesis

**Top 3 Most Profitable Products:**

- *Dorito Corn Chp Supreme*: 40,352.0
- *Smiths Crnkle Chip Orgnl Big Bag*: 36,367.6
- *Smiths Crinkle Chips Salt & Vinegar*: 34,804.2

**Loyal Customer Characteristics:**

- **Life Stage Distribution:**  
  - Older Families: 36.94%  
  - Young Families: 31.16%  
  - Older Singles/Couples: 12.35%  
  - Retirees: 6.72%  
  - Midage Singles/Couples: 6.71%  
  - Young Singles/Couples: 6.07%  
  - New Families: 0.06%

- **Premium Customer Distribution:**  
  - Budget: 40.69%  
  - Mainstream: 33.48%  
  - Premium: 25.83%

**Hypothesis for Customer Preference:**

Loyal customers primarily purchase *Dorito Corn Chp Supreme* and similar products. This may be driven by:
- Strong brand loyalty to particular snack brands.
- Regular consumption patterns leading to habitual purchases.
- Price sensitivity that aligns with their customer segment.
- High product availability in frequently visited stores.
