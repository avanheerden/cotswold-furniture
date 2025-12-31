# Retail Performance Optimisation: Unlocking £9.9M in Profit Potential

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Tableau](https://img.shields.io/badge/Tableau-Public-orange)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-yellow)

## 📊 Executive Summary
**Project Role:** Data Strategy & Analytics Lead  
**Outcome:** Identified a strategic roadmap to increase annual profit by **106%** (from £9.4m to £19.2m).

This project demonstrates how advanced analytics and Python-based modelling can transform raw transactional data into high-value strategic recommendations. By moving beyond basic reporting to **Price Elasticity Modelling** and **Customer Lifetime Value (CLV)** analysis, I diagnosed the root causes of margin erosion for a mid-sized furniture retailer.

[**> View the Interactive Tableau Dashboard**](https://public.tableau.com/app/profile/adriaan.van.heerden/viz/Cotswold/Dashboard-MAIN)  
[**> Download the Strategic One-Pager (PDF)**](Link_to_your_PDF_file.pdf)

---

## 💼 The Business Challenge
The client possessed **34 months of transactional history** (6,000+ orders) but lacked the in-house expertise to leverage it. Despite being data-rich, the business faced:
* **Eroding Margins:** A generic discounting strategy was bleeding profit.
* **Seasonal Slumps:** A consistent **21% year-on-year sales decline** in January.
* **Operational Waste:** Returns were costing the business **6.6% of total profit** (£619k/year).

---

## 💡 Key Strategic Insights
Using Python for data mining and statistical analysis, I identified four key levers to double company valuation:

### 1. Pricing Strategy: Plugging £1.45M in Leakage
* **The Insight:** Statistical analysis revealed that 9 out of 10 discounted products were **price inelastic**.
* **The Evidence:** Discounting "Wardrobes" saved customers £325k but resulted in a **-0.01 elasticity score**, effectively giving away margin with no volume increase.
* **The Action:** Immediate removal of discounts on unresponsive inventory.

### 2. Geographical Efficiency: A £5.3M Opportunity
* **The Insight:** The North East region generates **£0.41 per capita profit**, dwarfing the **£0.13** generated in London and the South East.
* **The Action:** Replicating the North East's efficiency in high-population regions unlocks massive scalability.

### 3. Customer Loyalty: The "Vital Few"
* **The Insight:** The business is heavily transactional but relies on a tiny cohort of high-value repeaters. The top 10 customers alone account for **52% of all sales**.
* **The Action:** A tiered **Loyalty Programme** to convert "Occasional" buyers into "High-Value Repeats," projected to yield a **£2.6m ROI**.

---

## 🛠️ Methodology & Tech Stack

### 1. Data Processing (Python/Pandas)
* **Data Cleaning:** Handled 6,000 rows of raw sales data, ensuring data quality score of 100%.
* **Feature Engineering:** Created new features for `Seasonality`, `Delivery_Lag`, and `Discount_Depth`.

### 2. Statistical Modelling (SciPy/Scikit-Learn)
* **Price Elasticity of Demand (PED):** calculated the correlation between price drops and volume increases for every SKU to determine discount sensitivity.
* **Correlation Matrix:** Mapped the relationship between `Discount %` and `Profit Margin` (Correlation: 0.405).

### 3. Visualization (Tableau/Matplotlib)
* **Tableau:** Built an interactive executive dashboard for C-suite stakeholders to filter by Region and Product.
* **Matplotlib/Seaborn:** Generated static charts for the "Discount Strategy Matrix" and "Waterfall Valuation Model."

---

## 📂 Repository Structure
```bash
├── data/
│   ├── cotswold_sales.csv                        # Original dataset (Synthetic/Dummy data)
│   └── cotswold_enriched_sales_data.csv          # Enriched dataset used for analysis & modelling
├── notebooks/
│   ├── cotswold.ipynb                            # QA and pre-processing, exploratory analysis, price elasticity & strategy logic 
├── reports/
│   ├── Cotswold Furniture Case Study.pdf         # The one-page summary
│   └── Cotswold Furniture Case Study.pptx        # The detailed report
│   └── Dataset Quality Report.md                 # Dataset quality report
└── README.md
└── License.md
