# AI-powered_River_Pollution_Monitoring

This project leverages machine learning and data analytics to monitor and assess river pollution levels in major Indian rivers — **Ganga**, **Sangam**, and **Yamuna**. Using water quality parameters like pH, DO, ORP, Temperature, and Conductivity, the system classifies water pollution status (e.g., *Very Poor*, *Fair*) and visualizes trends with clear, interactive graphs.

---

## 🔍 Features

- ✅ Cleaned and merged real-world river water data (CSV & JSON)
- ✅ Supervised ML model (Random Forest) for pollution classification
- ✅ Visual analytics: box plots, scatter plots, bar graphs
- ✅ Predictive insights on unseen data
- ✅ Exportable graphs and model files for report usage
- 🧠 Ready for integration with Streamlit, Power BI, or Dash

---

## 🧪 Data Sources

- `ganga.csv` – Water quality readings from River Ganga
- `sangam.csv` – Readings from Sangam confluence point
- `annotations.json` – Pollution-labeled image data for Yamuna

---

## 🧠 Machine Learning

- Features: `DO`, `pH`, `ORP`, `Cond`, `Temp`, `WQI`
- Target: `Status` (Very Poor, Fair, etc.)
- Model: `RandomForestClassifier`
- Output: Trained model saved as `rf_model.pkl`

---

## 📊 Visualizations

- DO vs WQI (bubble size = Temp)
- pH vs Status (boxplot)
- WQI vs Temperature
- ORP vs Conductivity by river
- Average WQI per river

All plots are export-ready and usable in research reports.

---

## 🛠️ Tech Stack

- Python 3.10+
- pandas, seaborn, matplotlib, plotly
- scikit-learn, joblib
- Jupyter Notebook / Google Colab

---

## 🚀 How to Run

1. Clone the repo  

git clone https://github.com/your-username/river-pollution-monitor.git
cd river-pollution-monitor


2. Open the Jupyter notebook or Colab link provided

3. Run all cells to train model, visualize, and generate reports

---

## 📄 Report Use

This project is suitable for:
- DRDO internship submissions
- IEEE-style student papers
- Academic ML/AI projects
- Smart city environmental monitoring demos

---

## 📫 Contact

**Chanchal Vishwakarma**  
📧 [chanchalvish2411@gmail.com]  
🔗 [https://linkedin.com/in/chanchalvish-a01858269]  
📁 Portfolio: [https://chanchal2411.github.io/html-css-js-portfolio]

---

## 📜 License

This project is open-source and available under the MIT License.
