**Solar Energy Analysis - Week 1 Challenge**  
*10 Academy Data Engineering Initiative*  

**Project Scope**  
This repository contains work for 10 Academy's Week 1 Solar Energy Challenge, focusing on processing and evaluating solar datasets from African nations to aid renewable energy decision-making. Structured tasks are documented below for transparency and reproducibility.  

---

### ✔️ Phase 1: Version Control & Collaboration Setup  
**Purpose**  
Establish a Git-managed collaborative environment for organized code development.  

**Deliverables**  
- Set up Git repo with *.gitignore* (excluded CSV/venv/IPYNB checkpoints)  
- Configured Python virtual environment using *requirements.txt*  
- Implemented branch-per-task workflow (feature/task branches)  
- Maintained merge history with rebased commits  
- Hosted repository on GitHub  

---

### ✔️ Phase 2: Dataset Transformation & Insights  
**Goal**  
Transform and investigate solar datasets to enable comparative analysis across nations.  

**Target Countries**  
- Togo  
- Benin  
- Sierra Leone  

**Methodology**  
*Branch Strategy*  
- Country-specific branches (e.g., *eda-benin*)  

*Notebook Workflows*  
- `benin_analysis.ipynb`, `sirraleone_analysis.ipynb`, `togo_analysis.ipynb`  

*Data Assessment*  
- Generated statistical summaries (mean, percentiles)  
- Detected columns exceeding 5% missing data threshold  

*Data Refinement*  
- Addressed outliers via Z-score filtering (threshold: ±3σ)  
- Median imputation for incomplete records  
- Cleaned outputs: *data/[country]_processed.csv*  

*Exploratory Insights*  
- Temporal trends: GHI/DNI/DHI/Tamb fluctuations  
- Distribution analysis for sensor anomalies/wind patterns  
- Heatmaps for variable correlations  
- Bubble charts (GHI vs Tamb with RH/BP context)  
- Wind direction roses and pressure histograms  

*Cleaning Validation*  
- ModA/ModB performance comparisons pre/post-processing  
- Flag-based visualizations for data quality impact  

---

**Environment Setup**  
1. Clone repo:  
`git clone https://github.com/abdulmunimjemal/solar-challenge-week1.git && cd solar-challenge-week1`  

2. Configure virtual environment:  
```bash  
python -m venv solar_env  
source solar_env/bin/activate  # Linux/macOS  
pip install -r requirements.txt  
```  

**Repository Layout**  
```
├── analysis/          # Exploration notebooks  
├── modules/          # Core Python scripts  
├── utilities/        # Helper scripts  
├── tests/            # Test cases  
└── data/             # Raw/processed datasets (*.gitignored)  
```