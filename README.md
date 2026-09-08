# Seasonal Agricultural Performance Analysis

## Project Overview

This project is a comprehensive exploratory data analysis (EDA) of a seasonal agricultural performance dataset covering **4,000 farm-level records**. It investigates how crop yield, profitability, and resource usage vary across different seasons, crops, irrigation methods, and environmental conditions, with the goal of surfacing actionable, evidence-based insights for improving farm productivity and sustainability.

The dataset captures farming practices, environmental conditions, crop production, resource usage, and economic performance across three growing seasons — **Kharif, Rabi, and Zaid**.

## Project Goal

To investigate how agricultural performance varies across seasons and identify meaningful patterns, trends, relationships, and differences within the data — ultimately translating statistical findings into practical recommendations for farmers and policymakers.

## Tools & Libraries

- **Python**
- **Pandas** — data cleaning, wrangling, and aggregation
- **NumPy** — numerical computations
- **Matplotlib** — static data visualizations
- **Seaborn** — statistical visualizations and styling

## Dataset

The dataset (`seasonal_agriculture_performance_dataset.csv`) contains farm-level records with the following categories of attributes:

- **Environmental factors**: Rainfall, temperature, soil moisture, soil pH
- **Farming practices**: Irrigation method, fertilizer/pesticide usage, seed quality
- **Production metrics**: Crop type, yield (tonnes/ha), water efficiency
- **Economic metrics**: Total cost, revenue, profit, market price
- **Categorical context**: Season, crop, irrigation method

## Analysis Workflow

1. **Data Loading & Inspection** — Verified structure, shape, and data types of the dataset.
2. **Data Cleaning** — Identified and imputed missing values (crop-grouped median imputation) and removed duplicate records.
3. **Descriptive Statistics** — Summarized numerical and categorical variables.
4. **Outlier Detection** — Used the IQR method to flag extreme values in farm area, rainfall, yield, and profit.
5. **Univariate Analysis** — Explored individual distributions of yield, season, and irrigation method adoption.
6. **Bivariate Analysis** — Compared average yield by crop and water efficiency by irrigation method.
7. **Multivariate Analysis** — Analyzed the relationship between rainfall and profit, segmented by season.
8. **Correlation Analysis** — Built a correlation heatmap across key agricultural drivers (rainfall, temperature, soil moisture, fertilizer, pesticide, seed quality, yield, profit, water efficiency).
9. **Seasonal Comparisons** — Compared mean yield and profit across Kharif, Rabi, and Zaid seasons.
10. **Custom Analyses** — Additional student-designed investigations, including irrigation method vs. profitability and seed quality vs. yield.
11. **Insights, Recommendations & Limitations** — Documented key findings, actionable recommendations, and dataset limitations, concluding with an overall summary.

## Key Insights

- Climatic and soil baselines (rainfall, temperature, soil moisture, pH) are fairly balanced across farms, while **yield and profit are heavily right-skewed**, driven by a small subset of high-performing farms.
- **Sugarcane** dramatically outperforms other crops in average yield.
- **Flood irrigation** is the most widely adopted method (~33% of farms) but has the **lowest water efficiency**, while rainfed methods are the most efficient.
- **Kharif season** consistently leads in both average yield and profit; **Zaid season** shows the weakest performance, with a negative average profit.
- Profitability appears more closely tied to **resource-use efficiency and input quality** (irrigation method, seed quality, precision fertilizer use) than to raw input volume.

## Recommendations

1. Incentivize the transition from flood to drip/micro-irrigation, especially for water-intensive crops like rice and sugarcane.
2. Promote precision soil testing to curb over-fertilization and reduce losses linked to excessive input use.
3. Support certified seed subsidies and Integrated Pest Management (IPM) practices to improve yield consistency and reduce crop loss.

## Limitations

- The dataset is **cross-sectional** (single-season snapshots), not longitudinal, limiting multi-year trend analysis.
- **Supply chain and logistics costs** (transportation, storage, mandi fees) are not captured in total cost figures.
- Missing values were handled via **crop-grouped median imputation**, which may smooth over localized microclimatic variation.
- Relationships between soil chemistry variables and yield are assumed to be largely linear, which may oversimplify real-world agronomic dynamics.

## Conclusion

Agricultural profitability in this dataset depends more on **resource-use efficiency and precision management** than on the sheer volume of inputs used. Farms relying on flood irrigation, uncertified seeds, and reactive pesticide use show significant financial losses, while those adopting water-efficient irrigation, quality seeds, and disciplined input practices achieve more stable margins. Future efforts should prioritize **micro-irrigation adoption** and **balanced, data-driven input application** to improve both yield and profitability sustainably.

## How to Run

1. Ensure Python 3.x is installed along with `pandas`, `numpy`, `matplotlib`, and `seaborn`.
2. Place `seasonal_agriculture_performance_dataset.csv` in the same directory as the notebook.
3. Open `code.ipynb` in Jupyter Notebook / JupyterLab and run all cells sequentially.
