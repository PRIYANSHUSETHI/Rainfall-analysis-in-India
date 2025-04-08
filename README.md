
# 🌧️ Rainfall Trend Analysis in India (1901–2015)

A data analytics and visualization project focused on analyzing rainfall trends across India from 1901 to 2015. This end-to-end exploratory pipeline combines climate science insights, statistical modeling, and machine learning to understand long-term patterns, detect anomalies, and forecast future rainfall.

---

## 📌 Key Features

- 📈 Trend and seasonality analysis
- 🔍 Climate change detection via change point analysis
- 📊 Rainfall volatility and anomaly detection
- 📉 Rolling averages and drought detection
- 📌 Feature importance via LightGBM
- 🔮 Time series forecasting using Facebook Prophet
- 🔥 Anomaly heatmaps and calendar visualizations
- 🤖 KMeans clustering of rainfall behavior

---

## 🧰 Libraries Used

| Library | Purpose |
|--------|---------|
| `pandas`, `numpy` | Data manipulation and numerical computation |
| `matplotlib`, `seaborn` | Static data visualization |
| `plotly` | Interactive and aesthetically enhanced charts |
| `ruptures` | Change point detection for climate regime shifts |
| `scipy.stats` | Correlation, distribution fitting, EVT |
| `sklearn` | Machine learning (Isolation Forest, KMeans, LightGBM) |
| `prophet` | Forecasting future annual rainfall |
| `calplot` | Calendar heatmap of rainfall intensity |

---

## 📂 Dataset

- **Source:** [IMD Historical Rainfall Data](https://data.gov.in/)
- **Timeframe:** 1901–2015
- **Columns:** Monthly rainfall (JAN–DEC), seasonal aggregates, and annual totals (ANNUAL)

---

## 📊 Visualizations & Analytics

### 1. **Annual Rainfall Trend Line**
- Plots historical trend from 1901–2015.
- Includes a line for mean rainfall.

### 2. **Monthly & Seasonal Average Rainfall**
- Bar plots show the most and least rainy months.
- Seasonal breakdown: Jan–Feb, Mar–May, Jun–Sep (Monsoon), Oct–Dec.

### 3. **Climate Change Impact**
- Rolling 10-year average plotted to visualize long-term shifts.
- Detects climate regime shifts using `ruptures`.

### 4. **Extreme Value Theory**
- Fits GEV distribution to annual rainfall maxima to assess risk of extreme events.

### 5. **Rainfall Volatility Index**
- 5-year rolling standard deviation captures inter-annual variability.

### 6. **Anomaly Detection**
- Uses **Isolation Forest** to detect:
  - Unusual annual rainfall years
  - Outlier months across the century
- Heatmaps highlight monthly anomalies (z-score based)

### 7. **Feature Importance (LightGBM)**
- Trained on monthly data to predict annual rainfall.
- Feature importance scores visualize which months contribute most.

### 8. **Forecasting with Confidence**
- Future rainfall predicted using **Prophet**.
- 95% Confidence Interval shaded.
- Annotated inflection points (e.g., post-2025 regime change?)

### 9. **Rainfall Clustering**
- KMeans classifies years into **Dry**, **Normal**, and **Wet**.
- Based on scaled seasonal and annual patterns.

### 10. **Calendar Heatmap**
- Daily-level approximation of monthly rainfall for a chosen year.
- Uses `calplot` to visualize distribution.

---

## 🔁 How to Run

```bash
# Clone the repository
git clone https://github.com/your-username/rainfall-trend-analysis.git
cd rainfall-trend-analysis

# Install dependencies
pip install -r requirements.txt
```

### Sample `requirements.txt`
```
pandas
numpy
plotly
seaborn
matplotlib
ruptures
scikit-learn
prophet
calplot
```

---

## 📌 Notebook Highlights

Each analytical section is modular and well-commented:
- Easy to extend with new forecasting models
- Can integrate real-time data from IMD or NOAA
- Ready for dashboard deployment via Streamlit or Dash

---

## ✨ Future Enhancements

- Regional analysis (state-wise, city-wise)
- Rainfall vs. temperature correlation
- El Niño/La Niña impact using ENSO/IOD indices
- Streamlit dashboard for real-time interaction

---

## 📬 Contact

For queries or collaborations, feel free to reach out via [yourname@email.com] or raise an issue.
