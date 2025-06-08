## Project Overview

The Coral Reef Evaluation and Monitoring Project (CREMP) Analysis is a comprehensive investigation of long‑term reef health trends in the Florida Keys National Marine Sanctuary. By integrating CREMP biological surveys (1996–2023) with environmental metrics (water quality, temperature, air pollution), this work characterizes spatial and temporal dynamics of stony corals, octocorals, and associated benthic communities, and builds predictive models to inform conservation strategies.

## Objectives

1. **Assess Reef Health**: Quantify changes in live coral and octocoral cover, species richness, and clustering over 27 years.
2. **Evaluate Drivers**: Examine relationships between coral metrics and environmental stressors (temperature, disease, sedimentation, pollution).
3. **Identify Refugia**: Highlight sites exhibiting recovery or resilience for targeted protection.
4. **Predict Future Trends**: Develop LSTM and Prophet forecasting models to project benthic cover over the next five years.
5. **Recommend Actions**: Offer data‑driven conservation and policy recommendations.

## Report Structure

* **Introduction**: Context on coral biodiversity, threats, and CREMP monitoring framework.
* **Exploratory Analysis**: Station‑level trends in percent cover and species richness.
* **Correlations & Spatial Patterns**: Statistical tests on living tissue area, Ripley’s K clustering, richness‑density relationships.
* **Environmental Drivers**: Temperature–disease links, sedimentation impacts, subregional comparisons.
* **Predictive Modeling**: LSTM architecture and performance; 5‑year forecasts.
* **Conclusions & Recommendations**: Key insights and actionable management strategies.

## Key Findings

* **Widespread Decline**: Over 64% of stations show net losses in live coral cover (1996–2023), driven by thermal stress and local stressors.
* **Octocoral vs. Stony Coral Response**: Octocoral density increases at \~0.8 colonies/m² per 1 °C rise, while stony coral density declines by \~0.15 colonies/m² per 1 °C.
* **Regime Shift**: Post‑2017 collapse of canopy‑forming species (Eunicea calyculata) and compensatory rise of robust taxa (E. flexuosa, Pseudopterogorgia americana).
* **Clustering Intensification**: Ripley’s K indicates a 56% increase in local clustering (500 m) over 25 years.
* **Richness–Density Link**: Pearson’s r ≈ 0.55; each extra species correlates with \~20–25 additional colonies per area.
* **Environmental Sensitivities**: UK subregion shows highest disease sensitivity to temperature; sedimentation reduces richness by \~14% per 10% increase.
* **Forecast Accuracy**: LSTM and Prophet models achieve median MAEs of 0.02–0.05 cover units, enabling reliable short‑term projections.

## Predictive Modeling

* **LSTM Architecture**:

  * Two stacked LSTM layers (32 units each) with dropout and GlobalAveragePooling1D.
  * Trained on 24‑month look‑back windows for four benthic groups.
  * Achieved RMSEs of 0.043–0.064 and MAPE of 35–66% across targets.

* **Prophet Forecasts**:

  * Monthly forecasts of percent cover for stony coral, macroalgae, octocoral, and porifera.
  * Uncertainty bands within ±15% of mean cover.

## Recommendations

1. **Protect Refugia**: Expand zoning around Alligator and Rawa reefs.
2. **Enhance Disease Surveillance**: Real‑time, temperature‑linked monitoring in UK and MK.
3. **Reduce Local Stressors**: Implement nutrient and sediment runoff mitigation.
4. **Integrate Forecasts**: Use annual model updates in adaptive management cycles.
5. **Restore Structural Diversity**: Focus on canopy‑forming species in nursery and outplanting programs.
6. **Secure Funding & Collaboration**: Establish multi‑agency partnerships and environmental trust funds.

## Data & Methods

* **Data Sources**: CREMP surveys, NOAA disturbance monitoring, EPA water quality, state/federal air pollution stations.
* **Statistical Analyses**: Shapiro–Wilk, Levene’s, ANOVA, Kruskal–Wallis, Pearson/Spearman correlations, GLMs (Poisson, Negative Binomial).
* **Spatial Analysis**: Ripley’s K‑Function to quantify clustering at multiple scales.
* **Modeling Tools**: Python (pandas, scikit‑learn, TensorFlow/Keras, Prophet).


## License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.

---

*Happy reefing!*
