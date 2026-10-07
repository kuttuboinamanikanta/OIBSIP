# Unemployment Analysis with Python 📊

## Overview
This project is part of the Oasis Infobyte Data Science internship. The objective is to perform Exploratory Data Analysis (EDA) on India's unemployment data to uncover regional and temporal trends, with a specific focus on the economic impact of the COVID-19 pandemic and lockdowns.

## Tech Stack
* **Language:** Python 3.x
* **Environment:** Jupyter Notebook
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`

## Dataset
The project utilizes the **"Unemployment in India"** dataset sourced from Kaggle. It contains monthly data on the estimated unemployment rate, estimated employed count, and estimated labor participation rate across various Indian states and regions (Rural vs. Urban) from 2019 to 2020.

*Note: The raw dataset contains structural irregularities (leading spaces in column headers, trailing empty rows, string-based dates) which are systematically cleaned in the initial stages of this notebook.*

## Project Workflow & Visualizations
1. **Data Cleaning & Preprocessing:** 
   * Stripped whitespace from column names.
   * Dropped completely null rows.
   * Converted string dates into workable Pandas `datetime` objects.
2. **Temporal Analysis (Time-Series):** 
   * Plotted a line chart tracking the unemployment rate of major states (Delhi, Maharashtra, Uttar Pradesh) over time.
   * Highlighted the massive spike in unemployment during the April/May 2020 COVID-19 lockdowns.
3. **Regional Analysis:** 
   * Created a bar chart visualizing the Top 10 Indian states with the highest average unemployment rates (e.g., Tripura, Haryana, Jharkhand).
4. **Correlation Analysis:** 
   * Generated a correlation heatmap to identify the inverse relationship between the Unemployment Rate and the Estimated Employed workforce.
5. **Pre-COVID vs. Post-COVID Impact:** 
   * Split the dataset at the March 24, 2020 lockdown date.
   * Calculated and visualized the absolute surge in national average unemployment before and after the lockdowns.
6. **Demographic Divide:** 
   * Compared average unemployment trends between Rural and Urban areas, revealing that Urban sectors suffered a sharper, more sustained job loss crisis during the pandemic peak.

## Key Findings
* **The Lockdown Shock:** Unemployment rates jumped drastically from a pre-pandemic average of ~9% to localized peaks exceeding 40% (e.g., in Delhi) immediately following the March 2020 lockdowns.
* **The Urban Crisis:** Urban areas consistently experienced higher unemployment rates than rural areas, largely due to rural populations falling back on the agricultural sector while urban manufacturing and gig economies halted.
* **Systemic Regional Issues:** States like Tripura and Haryana maintained high average unemployment rates throughout the entire 2019-2020 period, indicating structural labor challenges independent of the pandemic.

## How to Run This Project Locally
1. Clone this repository to your local machine.
2. Ensure the `Unemployment in India.csv` file is located in the same directory as the notebook.
3. Install the required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter