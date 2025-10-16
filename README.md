# 🔋 Predictive Modeling of Carbon Intensity with Environmental Impact Analysis

This project implements a real-time system to monitor and forecast carbon intensity (gCO2/kWh) in electricity generation using open data. It applies machine learning models, dynamic threshold anomaly detection, and environmental impact scoring to support green decision-making and promote sustainability.

📄 **Published in:**  
IEEE International Conference on Data Science, Agents & Artificial Intelligence (ICDSAAI 2025) · May 29, 2025  
🔗 [Read on IEEE Xplore](https://ieeexplore.ieee.org/document/11011703)

---

## 🧠 Features

- 📡 Real-time carbon intensity data ingestion via API  
- 🔮 Future prediction using Random Forest & SGD (R²: 0.98)  
- ⚠️ Dynamic anomaly detection with Isolation Forest  
- ♻️ Environmental Impact Scoring (Low / Medium / High)  
- 💡 Smart sustainability pathway recommendations  
- 📈 Rolling mean-based trend analysis  
- 📊 Factor contribution visualization (e.g. coal, imports)  

---

## 📊 Methodology

1. **Data Source**: UK Carbon Intensity API 
2. **Modeling**:
   - Random Forest Regressor for carbon prediction  
   - SGD Regressor with polynomial features for complex time trends  
3. **Anomaly Detection**:
   - Isolation Forest for point-wise anomaly scores  
   - Dynamic thresholding via rolling stats to detect spikes  
4. **Environmental Impact Score**:
   - Categorized into low (0-30), medium (31-60), and high (>60)  
   - Recommendations mapped to severity  
5. **Fuel Factor Analysis**:
   - Coal, Gas, Oil, Imports — ranked by % contribution to emissions  

---

## 🧠 Tech Stack

- **Frontend:** Streamlit  
- **Backend:** Python, Requests  
- **ML Models:** Random Forest, Isolation Forest, Polynomial Regression  
- **APIs Used:** [UK Carbon Intensity API](https://carbon-intensity.github.io/)  
- **Visualization:** Matplotlib, Seaborn, pandas  

---

## 🚀 Deployment

The entire system is implemented using **Streamlit** for a fast and interactive frontend. Charts, metrics, and maps update every minute based on API data.

### 🔄 Installation

```bash
# Clone the repository
git clone https://github.com/paraspatil11/Predictive-modeling-of-carbon-intensity-with-Environmental-impact-analysis.git
cd Predictive-modeling-of-carbon-intensity-with-Environmental-impact-analysis

# Install dependencies
pip install -r requirements.txt

# Run the Streamlit App
streamlit run app.py
