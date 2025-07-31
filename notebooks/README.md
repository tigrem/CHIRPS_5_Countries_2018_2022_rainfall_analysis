# CHIRPS 5 Countries Rainfall Analysis (2018-2022)

## Project Overview

This project analyzes monthly rainfall data from 2018 to 2022 across various regions in five eligible countries (Ethiopia, Kenya, Somalia, etc., as per the CHIRPS dataset). The primary goal is to identify noticeable trends, seasonal patterns, and anomalies in rainfall, understand their potential influence on crop yields and farming practices, and propose additional datasets to enhance agricultural and climate decision-making.

## Dataset

The dataset used for this analysis is `CHIRPS_5_Countries_2018_2022.csv`, containing monthly rainfall (mm) aggregated by year, month, country, and region.
Data source: [DE Africa CHIRPS](https://registry.opendata.aws/deafrica-chirps/) (Note: The specific file was provided as part of the assignment).

## Project Structure

The project is organized as follows:
CHIRPS_5_Countries_2018_2022_rainfall_analysis/
├── Data/
│   └── CHIRPS_5_Countries_2018_2022.csv  # The rainfall dataset
├── notebooks/
│   └── Rainfall_Analysis.ipynb         # Jupyter Notebook with the analysis
│   └── README.md                       # (Optional) README for the notebooks folder
├── src/                                  # For any reusable Python scripts (currently empty)
├── tests/                                # For unit tests (currently empty)
├── venv/                                 # Python virtual environment
├── .gitignore                            # Git ignore file
├── init.py                           # Python package marker
├── LICENSE                               # Project license (e.g., MIT, Apache 2.0)
├── README.md                             # This README file
└── requirements.txt                      # List of project dependencies


## Analysis Performed

The `Rainfall_Analysis.ipynb` Jupyter Notebook covers the following steps:

1.  **Setup and Data Loading:**
    * Imports necessary libraries (pandas, matplotlib, seaborn).
    * Loads the `CHIRPS_5_Countries_2018_2022.csv` file, handling potential encoding issues.
2.  **Initial Data Inspection:**
    * Displays the first few rows, data types, and descriptive statistics.
    * Checks for missing values.
3.  **Data Cleaning and Preprocessing:**
    * Ensures correct data types for 'Year', 'Month', and 'Rainfall_mm'.
    * Creates a `Date` column for time-series analysis.
    * Handles any missing rainfall values (imputes with 0).
    * Includes a fix for the `Glyph 146` UserWarning by setting `matplotlib.rcParams['font.family'] = 'DejaVu Sans'`.
4.  **Rainfall Trend, Pattern, and Anomaly Identification:**
    * **Overall Trend:** Visualizes total monthly rainfall across all regions over the 5-year period.
    * **Seasonal Patterns:** Shows average monthly rainfall to identify typical wet/dry seasons.
    * **Country-Specific Trends:** Compares total monthly rainfall for each country.
    * **Anomalies:** Identifies unusually high or low rainfall months using Z-scores, indicating potential flood or drought events.
    * **Regional Trends within Countries:** Generates separate plots for each country, showing rainfall trends across its specific regions, highlighting localized variations.
5.  **Influence on Crop Yields & Farming Practices:**
    * Discusses how observed rainfall variability (droughts, floods, seasonal shifts, unpredictability) can impact crop yields and necessitate adaptive farming practices.
6.  **Proposed Additional Dataset:**
    * Suggests combining the rainfall data with **Crop Yield Data** to enhance agricultural and climate decision-making, explaining the rationale and benefits.

## How to Run the Project

1.  **Clone the Repository:**
    ```bash
    git clone <https://github.com/tigrem/CHIRPS_5_Countries_2018_2022_rainfall_analysis.git>
    cd CHIRPS_5_Countries_2018_2022_rainfall_analysis
    ```
2.  **Place the Dataset:**
    Ensure the `CHIRPS_5_Countries_2018_2022.csv` file is placed inside the `Data/` directory.
3.  **Create and Activate Virtual Environment (Recommended):**
    ```bash
    python -m venv venv
    # On Windows:
    .\venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```
4.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
5.  **Run Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    This will open Jupyter in your web browser. Navigate to the `notebooks/` directory and open `Rainfall_Analysis.ipynb`.
6.  **Execute Cells:** Run all the cells in the notebook sequentially to see the analysis and visualizations.

## Requirements

The necessary Python libraries are listed in `requirements.txt`.

## License

*(Choose a license, e.g., MIT, Apache 2.0, or state "Proprietary" if not open-source)*

## Contact

For any questions or suggestions, please contact tigremsahilu@gmail.com.