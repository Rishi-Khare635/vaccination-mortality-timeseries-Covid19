# COVID-19 Vaccination Rollout and Death Rate Trends: A Cross-Income Statistical Analysis

A statistical analysis investigating whether the rate of COVID-19 vaccination rollout correlated with a reduction in death rates across countries, and whether this pattern differs between high-income and low-income nations.

## Research Question

Did the rate of COVID-19 vaccination rollout correlate with a reduction in death rates across countries, and does this pattern differ between high-income and low-income nations?

## Dataset

* **Source:** Our World in Data (OWID)
* **Dataset:** COVID-19 Vaccinations dataset (vaccinations, deaths, GDP, and income classification by country and date)
* **Link:** https://ourworldindata.org/covid-vaccinations
* **Sampling method:** Stratified random sampling — 5 high-income and 5 low-income countries, selected from an eligible pool filtered by data completeness (≤88% missing vaccination data), using World Bank income classifications
* **Final sample:** Afghanistan, Ethiopia, Guinea, Malawi, Uganda (low-income); Antigua and Barbuda, Belgium, Denmark, Norway, Seychelles (high-income)

## Key Findings

* Both income groups showed a statistically significant reversal in death trends — rising before vaccination rollout, declining after (Mann-Kendall test, p ≈ 0 for all countries)
* Low-income countries showed **more consistent** declining trends (stronger Tau values), likely due to simpler, single-wave death curves rather than stronger vaccination effectiveness
* High-income countries showed a **faster** rate of decline (steeper Sen's slope), plausibly linked to greater healthcare access and infrastructure
* High-income countries had consistently **higher peak death rates** than low-income countries, with no overlap between groups — though whether this reflects genuine demographic differences (e.g., population age structure) or underreporting in lower-income countries' health systems remains unresolved
* Vaccination reporting completeness was substantially worse for low-income countries (80-87% missing) than for most high-income countries, a limitation documented throughout the analysis

## Project Structure

**data**
* raw data file (original CSV from Our World in Data)
* cleaned_covid_10countries.csv (processed data for final 10-country sample)

**notebooks**
* 01_cleaning.ipynb — data cleaning, stratified sampling, and rollout-relative time construction
* 02_eda.ipynb — exploratory data analysis and time series visualizations
* 03_analysis.ipynb — formal Mann-Kendall trend testing and Sen's slope analysis

**report**
* full written report (PDF)

## Tools Used

* Python
* pandas — data cleaning and manipulation
* matplotlib — time series visualization
* pymannkendall — Mann-Kendall trend test and Sen's slope estimation

## How to Run
Open notebooks in order: 01 → 02 → 03

## Author

Rishi Khare

Install dependencies and run the three notebooks in order:
