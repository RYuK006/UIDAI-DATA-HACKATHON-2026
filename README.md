# Aadhaar Enrolment Data Analysis
### **UIDAI Data Hackathon 2026**

## 📌 Project Overview
This project provides a comprehensive analytical framework for Aadhaar enrolment data. It includes tools for data profiling, temporal trend analysis, anomaly detection, and fraud risk scoring using machine learning. The goal is to uncover societal trends and identify suspicious enrollment patterns.

## 🚀 Features
- **Data Ingestion**: Automated loading and merging of large-scale enrolment CSV datasets.
- **Data Profiling**: Statistical summary and quality assessment (nulls, duplicates).
- **Temporal Analysis**: Visualization of enrollment trends and peak activity identification.
- **Anomaly Detection**:
    - **Demographic Skew**: Deviation from census age norms.
    - **Volumetric Spikes**: Z-score analysis for daily enrollment surges.
    - **Duplicate Detection**: Identification of redundant records.
- **Fraud Risk Scoring**: Grading records (Low/Medium/High/Critical) using a Gradient Boosting Classifier.

## 📂 Project Structure
```
UIDAI/
├── aadhaar_analysis.ipynb          # Main Jupyter Notebook
├── reproduce_analysis.py           # Python script for quick replication of trends
├── run_full_analysis.py            # Script to execute full anomaly detection pipeline
├── verify_notebook.py              # Utility to validate notebook syntax
├── detailed_analysis_report.txt    # Summary of key findings
├── priority_investigation_top1000.csv # Generated list of high-risk records
├── analysis_report.md              # Markdown report of methodology
└── api_data_aadhar_enrolment/      # Data Directory
    ├── *.csv                       # Source data files
    └── enrollment_trends_replicated.png
```

## 🛠️ Prerequisites
- Python 3.8+
- Jupyter Notebook
- Recommended libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

## ⚙️ Setup & Usage

### 1. Installation
Ensure you have the required dependencies installed:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 2. Running the Analysis
You can run the analysis using either the Jupyter Notebook or the provided Python scripts.

**Option A: Jupyter Notebook (Recommended)**
1. Open `aadhaar_analysis.ipynb` in Jupyter.
2. Ensure the `DATA_DIR` variable in the first code cell points to your data folder.
3. Run all cells to generate the analysis and risk scores.

**Option B: Python Script**
To generate the `priority_investigation_top1000.csv` and print findings directly to the console:
```bash
python run_full_analysis.py
```

## 📊 Key Outputs
- **`detailed_analysis_report.txt`**: A text file summarizing the 5.4M records analyzed, including the 10x spike observed on July 1st, 2025.
- **`priority_investigation_top1000.csv`**: A CSV containing the top 1,000 records flagged for immediate investigation, primarily concentrated in Uttar Pradesh and Kerala.
- **`aadhaar_analysis.ipynb`**: The complete interactive analysis implementation.
