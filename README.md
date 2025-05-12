# Data Center Sustainability Score

This repository contains the code, data pipeline, and analysis for a dynamic, ML-driven sustainability scoring system for U.S. data center siting along with the dataset used for this. The methodology integrates environmental, renewable, and infrastructure factors, using both supervised machine learning and reinforcement learning for adaptive, region-aware scoring.

---

## Overview

**Purpose:**  
To provide a reproducible, data-driven framework for evaluating and ranking potential data center locations in the United States based on sustainability criteria, including carbon emissions, water use, renewable energy profile, and infrastructure reliability.

---

## Features

- **CO₂ Emission Prediction:**  
  Uses XGBoost to estimate plant-level carbon emissions from fuel type, generation, and location.

- **Water Intensity Prediction:**  
  Uses LightGBM to predict water use intensity, leveraging plant, watershed, and grid features.

- **Dynamic Sustainability Scoring:**  
  Combines environmental impact, renewable profile, and infrastructure proximity with weights dynamically optimized by a reinforcement learning agent (PPO).

- **Geospatial Visualization:**  
  Plots sustainability scores across the U.S. with interactive maps for site selection.

---

## Methodology

1. **Data Ingestion:**  
   - Loads multiple tables from `Input_data.xlsx`, covering plant operations, grid regions, water and carbon intensities, and regional factors.

2. **Feature Engineering:**  
   - Calculates carbon intensity, water intensity, renewable fraction, grid stability, and infrastructure complexity.
   - Handles missing values and encodes categorical variables (target encoding for high-cardinality features like HUC8 ID).

3. **Machine Learning Models:**  
   - **XGBRegressor** for CO₂ emission prediction.
   - **LGBMRegressor** for water intensity.
   - **PPO RL agent** for dynamic weight allocation in the sustainability score.

4. **Scoring Formula:**  
   \[
   \text{Sustainability Score} = x \times (\text{Environmental Impact}) + y \times (\text{Renewable Profile}) + z \times (\text{Infrastructure Proximity})
   \]
   - Weights \(x, y, z\) are dynamically optimized per region, subject to constraints (each in [0.1, 0.7], sum to 1).

5. **Evaluation:**  
   - Model performance assessed with R² and MSE.
   - Rolling time series and spatial cross-validation to ensure robustness.

6. **Visualization:**  
   - Sustainability scores mapped using GeoPandas and Matplotlib.
   - Top 10 regions highlighted for optimal data center siting.

---

## Usage

1. **Install requirements:**
    All modules used are present in the first few cells of the notebook.

2. **Run the Notebook:**  
   Open `Data_Center_Sustainability_Score.ipynb` and execute all cells in order.

3. **Input Data:**  
   Place `Input_data.xlsx` in the same directory as the notebook.

4. **Outputs:**  
   - Sustainability score maps (`optimal_regions_map.png`)
   - Tables of ranked regions and model performance metrics

---

## Results
*See the notebook for detailed figures, maps, and top 10 region tables.*

