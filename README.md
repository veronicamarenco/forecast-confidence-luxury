# From Gut Feel to Forecast Confidence
## Demand Forecasting for Luxury & Beauty (Hermès, Dior, LVMH)

### The Problem
Luxury demand is driven by psychology: scarcity, celebrity endorsements, trend shifts, and seasonal spending patterns. 

Q4 spikes 300% (holiday gifting). A celebrity posts an Instagram photo with a Hermès Birkin and demand jumps 40%. Fashion weeks shift collections overnight. Summer drops 60% (vacations).

Your spreadsheet-based forecast can't capture any of this.

### The Solution
This tool identifies which signals actually drive luxury demand:
- **Trend breaks** (structural shifts vs. seasonal noise)
- **Scarcity effects** (waitlist length driving perceived value)
- **Seasonal patterns** (Q4, Chinese New Year, summer dips)
- **External signals** (celebrity moments, fashion weeks, TikTok trends)

### Key Features
- Prophet time series model (handles seasonality + trend)
- Signal decomposition (which signals matter?)
- Confidence intervals (when to trust the forecast)
- Streamlit dashboard (interactive forecasts)
- Scenario analysis (what-if simulations)

### How to Use

1. **Install dependencies**:
```bash
   pip install -r requirements.txt
```

2. **Explore the notebooks**:
   - `01_data_exploration.ipynb` — Load and understand the data
   - `02_seasonality_decomposition.ipynb` — Identify seasonal patterns
   - `03_trend_detection.ipynb` — Find trend breaks
   - `04_forecast_model.ipynb` — Build Prophet model

3. **Run the Streamlit dashboard**:
```bash
   streamlit run app/streamlit_dashboard.py
```

4. **Python and Python API
5. **:
```python
   from src.forecast_model import LuxuryDemandForecaster
   
   forecaster = LuxuryDemandForecaster(data='data/sample_hermes_demand.csv')
   forecast = forecaster.predict(horizon=52)  # 52 weeks ahead
   forecaster.plot_forecast()
```

### Dataset
- 4 years of weekly Hermès Birkin demand across colors and regions
- Includes known trend shifts (celebrity endorsements, fashion weeks)
- Seasonal patterns: Q4 peak (+300%), summer dip (-60%), Chinese New Year (+150%)
- External signals: luxury sentiment index, FX rates, competitor launches

### Core Insight
**"Luxury demand is driven by psychology and scarcity, not logic."**

This tool identifies trend breaks (structural shifts vs. seasonal noise) so you can react fast.

### Results
If you can predict a fashion trend 4 weeks early instead of 4 weeks late, you stock the right items before competitors do.

**Impact**: Forecast accuracy 85% → 92% = fewer expedites, lower safety stock, supply chain that trusts the plan.

### Technology Stack
- **Python**: Pandas, NumPy, Scikit-learn
- **Time Series**: Prophet (Facebook)
- **Visualization**: Plotly
- **Dashboard**: Streamlit
- **Database**: SQLite/CSV

### Files in This Repo
- `README.md` — This file
- `METHODOLOGY.md` — Detailed explanation of how the model works
- `notebooks/` — Jupyter notebooks (EDA, decomposition, modeling)
- `src/` — Python modules (data pipeline, model, forecasting)
- `app/` — Streamlit dashboard
- `data/` — Sample datasets

### Next Steps
1. Download sample data (or use your own Hermès/luxury sales data)
2. Run notebook 01 to explore
3. Run full Streamlit app to see interactive forecast
4. Adjust model parameters for your specific product line

### License
MIT

### Author
Veronica Marenco | Paris, France | [LinkedIn](https://linkedin.com/in/veronicamarenco)
