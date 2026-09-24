 HEAD
# Subsurface Capstone Project: Porosity Prediction from Well Logs

**Author:** Zedela Oluoch  
**Track:** Track A (Beginner)  
**Course:** Machine Learning for Petroleum Engineers & Geoscientists  
**Milestone 1 Status:** Complete (Due September 26, 2026)

---

## 📌 Project Overview
The goal of this project is to determine if a machine learning model can accurately predict Neutron Porosity (`NPHI_frac`) in a completely unseen, blind well using standard wireline physical logs. Predicting porosity automatically helps reservoir engineers and petrophysicists estimate hydrocarbon volumes in new wells without running expensive logging tools.

### Physical Log Features Used:
* **`GR_API` (Gamma Ray):** Reflects lithology variations (shale vs. sand sandstones).
* **`RHOB_gcc` (Bulk Density):** Inversely proportional to formation porosity.
* **`RT_ohmm` (Deep Resistivity):** Indicates fluid content and formation matrix changes.

*Note: Depth has been intentionally excluded as an input feature to eliminate spatial autocorrelation data leakage, ensuring the model relies purely on physical log relationships.*

---

## 📊 Milestone 1 Progress & Baselines

An honest **Leave-One-Well-Out split** was established by completely hiding **Well_B** from the training dataset to evaluate true deployment physics.

The initial baseline benchmarks logged on the blind test well are:
* **Naive Mean Baseline:** RMSE = `0.1107` | R² = `-0.0039`
* **Linear Regression Baseline:** RMSE = `0.0308` | R² = `0.9224`

---

## 🛠️ Repository Structure
```text
SUBSURFACE_CAPSTONE/
├── data/
│   └── well_log_data.csv        # Cleaned petrophysical wireline log dataset
├── notebooks/
│   └── capstone.ipynb           # Main workspace notebook (Milestone 1 code)
├── results/
│   └── capstone_results_log.csv # Automatically generated logging log tracker
└── README.md                    # Project documentation
```

---

## 🚀 How to Run this Project

1. **Clone the repository:**
   ```bash
   git clone <your-github-repo-link>
   cd SUBSURFACE_CAPSTONE
   ```

2. **Open the project workspace:**
   Open the main `SUBSURFACE_CAPSTONE` folder directly in VS Code.

3. **Run the code:**
   Navigate to `notebooks/capstone.ipynb` and select **Run All Cells** to reproduce our EDA, data split, and baseline models.

# ml-practice-notebooks
My private machine learning and deep learning files
 730982aa999219fdf4f6cbd657fa85b338094b9f
