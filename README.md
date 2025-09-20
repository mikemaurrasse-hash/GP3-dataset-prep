# Project 3: Deep & Wide Nets, RNNs, Kernels & Regressions — California Wine & Weather

This repository contains the deliverables for **Project 3**.  
It focuses on linking **California wine reviews** with **weather data** from growing seasons, then performing EDA, cleaning, and feature engineering.

---

## Structure

```
data/
  wine_ca_raw_clean.csv            # Cleaned California wine reviews
  ca_weather_growing_season.csv    # Aggregated growing season weather per AVA, year
  wine_weather_joined.csv          # Joined dataset (wine + weather features)
notebooks/
  Project3_CA_Wine_Weather.ipynb   # Main Colab-ready notebook
README.md
```

---

## How to Run

1. Open the notebook in **Google Colab** or Jupyter.  
   - Runtime: Python 3.10+ (GPU optional).  
   - Install dependencies via the first cell.  

2. Make sure to run the **seed cell** to fix randomness.

3. Data is fetched as follows:  
   - **Wine Reviews**: From public GitHub mirrors (FiveThirtyEight dataset).  
   - **Weather Data**: From [Meteostat API](https://meteostat.net) using `meteostat` Python client.  

4. Output CSVs are automatically saved into the `data/` folder.

---

## Engineering Notes

- **Wine dataset challenges**:  
  Mirrors occasionally move or rate-limit. Text includes inconsistent encodings. Vintage year is not a dedicated column and is parsed from `title`.  

- **Weather dataset challenges**:  
  Station coverage varies per AVA/year. Missing values (esp. precipitation) are imputed with medians and forward/back-fill.

---

## Next Steps

- Section 3–4 of the project will build models:  
  - Ridge/LASSO and kernel regressors  
  - Wide & Deep neural networks  
  - RNN over daily weather sequences  

---

*Generated README for coursework submission.*
