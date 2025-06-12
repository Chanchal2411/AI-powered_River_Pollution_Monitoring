# AI-Powered River Pollution Monitoring System

>  Built with Python · ML · Visual Analytics · Real Data from Ganga, Sangam & Yamuna

---

###  Problem Statement

Rivers are lifelines for agriculture, industry, and human survival. However, India's major rivers — **Ganga**, **Sangam**, and **Yamuna** — face critical pollution due to urbanization, industrial discharge, and sewage inflow. Traditional manual monitoring is slow and lacks predictive capabilities.

This project aims to build an **AI-powered pollution monitoring system** that uses:
- Sensor-based datasets
- Machine Learning classification
- Visual annotation of real images  
...to assess and predict **water quality status** in a scalable, data-driven way.

---

###  Tech Stack

| Layer              | Tools/Libraries                      |
|-------------------|--------------------------------------|
| Language           | Python 3.x                           |
| ML/AI              | Scikit-learn (Random Forest Classifier) |
| Data Handling      | Pandas, NumPy                        |
| Visualization      | Matplotlib, Seaborn, Plotly          |
| Image Annotation   | JSON (VIA/VGG Image Annotator format) |
| Dev Environment    | Google Colab / Jupyter Notebook      |
| Version Control    | Git, GitHub                          |

---

###  Data Sources

#### 🔹 Ganga & Sangam River Datasets
- Format: CSV
- Features:  
  `DO`, `pH`, `ORP`, `Temp`, `Cond`, `WQI`, `Status`
- Target: Water Quality Status (`Very Poor`, `Fair`, etc.)

#### 🔹 Yamuna River Visual Dataset
- Format: JSON (VGG Image Annotator)
- Image regions manually marked as:
  - `"polluted": "yes"`
  - `"polluted": "no"`

---

###  Model Overview

- **Model**: `RandomForestClassifier`
- **Input Features**:
  - Dissolved Oxygen (DO)
  - pH Level
  - Oxidation Reduction Potential (ORP)
  - Conductivity (Cond)
  - Temperature (Temp)
  - Water Quality Index (WQI)
- **Output**: Pollution status (`Very Poor`, `Fair`, etc.)
- **Performance**: Evaluated via Accuracy, Confusion Matrix, Classification Report

---

###  Architecture Diagram

```
         ┌──────────────┐
         │  CSV Inputs  │ <─ Ganga/Sangam data
         └────┬─────────┘
              │
        ┌─────▼─────┐
        │ Preprocess│
        └────┬──────┘
             ▼
      ┌──────────────┐       ┌────────────────────┐
      │Feature Matrix │       │ Annotated Images   │ <─ Yamuna JSON
      └────┬──────────┘       └────────┬───────────┘
           ▼                           ▼
    ┌──────────────┐           ┌──────────────┐
    │ ML Classifier│           │ Visual Labels│
    └────┬─────────┘           └──────────────┘
         ▼
 ┌───────────────┐
 │Predicted Status│
 └───────────────┘
         ▼
 ┌────────────────────────────┐
 │ Dashboard / Export to CSV  │
 └────────────────────────────┘
```

---

###  Sample Results & Visuals

|  Visualization                     |  Description                               |
|------------------------------------|--------------------------------------------|
| **DO vs WQI (Bubble Plot)**        | Bubble size = Temperature                  |
| **pH vs Status (Boxplot)**         | Shows distribution of pH by quality level  |
| **WQI vs Temperature (Scatter)**   | Identifies heat influence on pollution     |
| **ORP vs Cond (2D Scatter)**       | Shows chemical balance vs conductivity     |
| **Avg. WQI per River (Bar Chart)** | Compares overall pollution per river       |

---

###  How to Run

####  Option A: Google Colab (Recommended)
1. Open `AI_River_Monitoring_Colab.ipynb`
2. Upload:
   - `ganga.csv`
   - `sangam.csv`
   - `annotations.json`
3. Run all cells to:
   - Train the model
   - Predict water quality
   - Visualize trends
   - Export graphs + model

####  Option B: Jupyter Notebook
```bash
git clone https://github.com/<your-username>/river-pollution-monitor.git
cd river-pollution-monitor
jupyter notebook
```

---

###  Future Enhancements

-  **Live Monitoring via Drones/Satellites**
  - Integrate drone imagery or satellite data for real-time visual analysis

-  **IoT Sensor Integration**
  - Stream sensor data directly from river stations into the model

-  **Image Classification (CNN)**
  - Build deep learning models to detect polluted zones in Yamuna images automatically

-  **Cloud Dashboard**
  - Deploy the system with Streamlit or Power BI for government dashboards

---

###  Conclusion

This AI-based river pollution monitoring system provides:
- A **scalable model** trained on real-world environmental data
- Integration of **image-based visual validation**
- A foundation for **future smart water quality management systems**

---

###  Repository Structure

```
river-pollution-monitor/
├── data/
│   ├── ganga.csv
│   ├── sangam.csv
│   └── annotations.json
├── models/
│   └── rf_model.pkl
├── notebooks/
│   └── AI_River_Monitoring.ipynb
├── visuals/
│   └── plots/*.png
├── README.md
└── requirements.txt
```
