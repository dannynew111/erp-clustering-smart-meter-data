# erp-clustering-smart-meter-data
My repository for code used in behaviour-first two-stage framework for taking raw smart meter data from a large trial and using it to cluster households into distinct behavioural 'personas', each of which is then explained using socio-demographic and intrinsic lifestyle features to fully understand them and help create interventions.

# ERP Clustering of Smart Meter Data

## Project Description

This project analyses household energy consumption in London using publicly available smart meter datasets from 2012 (baseline year) and 2013 (dynamic pricing tariff year). By comparing a treatment group (on a dynamic tariff) against a control group, the analysis isolates the real effects of the pricing signals from external trends like weather or general energy price shifts.

The core of this project is the creation of detailed household personas through feature engineering and clustering. Key features were developed to measure:
*   **Price Responsiveness:** How households in the treatment group reacted to High, Normal, and Low price signals.
*   **Intrinsic Lifestyle:** Pre-trial (baseline) consumption habits, such as peak-to-off-peak ratios and daily consumption volatility.
*   **Socio-Economic Factors:** Financial and attitudinal characteristics derived from attached survey data.

By clustering households based on these features, this analysis provides an explanatory layer to the resulting personas. The final output is a strategic intervention toolkit designed to help energy providers effectively incentivize different user types to reduce their peak energy consumption, thereby alleviating stress on the national grid.

---

# Order of Execution

To reproduce the analysis and findings, the Jupyter Notebooks **must be executed in the following chronological order**. Each notebook is dependent on the output of the previous one.

1.  **`data_ingestion_v2.ipynb`**: This notebook handles the initial loading, cleaning, and merging of the raw smart meter consumption data and the household survey data.
2.  **`feature_engineering_v4.ipynb`**: This notebook constructs the core features for the analysis, including metrics for price responsiveness and intrinsic consumption patterns.
3.  **`EDA_visualisations_v4.ipynb`**: This notebook conducts exploratory data analysis, generating key visualizations to understand the distributions and relationships within the dataset.
4.  **`clustering_v4.ipynb`**: This notebook applies clustering algorithms to the engineered features to segment the households and create distinct user personas.
5.  **`advanced_stats_analysis.ipynb`**: This notebook performs the final statistical analysis on the generated clusters, interpreting the personas and formulating the strategic intervention toolkit.

---

# How to Run the Code

# 1. Data Source

The datasets used in this project are from the UK Data Service and are available at the following link:
[https://beta.ukdataservice.ac.uk/datacatalogue/studies/study?id=7857](https://beta.ukdataservice.ac.uk/datacatalogue/studies/study?id=7857)

**Important Note:** To access the consumption and survey data, you must create an account with the UK Data Service and register a project. The data files are too large to be uploaded directly to this GitHub repository. Once downloaded, they should be placed in the appropriate directory as referenced in the `data_ingestion_v2.ipynb` notebook.

# 2. Required Libraries

These notebooks were developed in a Google Colab environment. The analysis relies on standard Python data science libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`, etc.) as well as the following key `scikit-learn` modules. Ensure they are installed in your environment.

*   `sklearn.cluster`
*   `sklearn.mixture`
*   `sklearn.metrics`
*   `sklearn.decomposition`


