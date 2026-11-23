# Lab-Assignment-5-AI-Cyber-Security
# Explainable and Privacy-Aware AI Threat Alert

## 📌 Project Overview

This project demonstrates how Artificial Intelligence (AI) can be used in cybersecurity to detect potentially suspicious login activities while maintaining user privacy and providing explainable predictions.

A **Decision Tree Classifier** is used to classify login activities as `Normal` or `Suspicious`. The system also calculates prediction confidence, explains feature importance, performs sensitivity analysis, masks sensitive information, and generates responsible security alerts.

The project emphasizes explainable AI (XAI), privacy protection, and human-in-the-loop decision-making.

## 🎯 Objectives

- Detect potentially suspicious login activities using Machine Learning.
- Generate predictions with confidence scores.
- Identify important features influencing model decisions.
- Perform controlled sensitivity analysis.
- Protect sensitive information through data masking.
- Generate security alerts with severity levels and recommended actions.
- Ensure human review before taking high-risk security actions.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and analysis |
| Matplotlib | Data visualization |
| Scikit-learn | Machine Learning model |
| Decision Tree Classifier | Login activity classification |
| Google Colab / Jupyter Notebook | Development environment |

## 📊 Dataset Description

The model uses four numerical features to analyze login activities:

| Feature | Description |
|---|---|
| `failed_logins` | Number of unsuccessful login attempts |
| `login_hour` | Hour at which the login occurred |
| `new_device` | Indicates whether the login is from a new device (0 or 1) |
| `download_mb` | Amount of data downloaded in MB |

**Target Variable:**
- `Normal` – Login activity considered normal.
- `Suspicious` – Login activity considered potentially suspicious.

**Note:** This implementation uses a small illustrative training dataset because the original Lab 2 dataset was not included. Replace it with the original dataset when available for continuity and more meaningful evaluation.

## ⚙️ Project Workflow

1. **Data Preparation:** Prepare login activity records using the four numerical features.
2. **Model Training:** Train a Decision Tree Classifier with a maximum depth of 4.
3. **Baseline Predictions:** Classify five sample login records and calculate prediction confidence.
4. **Feature Importance:** Identify and visualize the features that contribute to model decisions.
5. **Sensitivity Analysis:** Change `failed_logins` from 2 to 8 while keeping other features fixed and compare predictions.
6. **Privacy Masking:** Mask account IDs and IP addresses before displaying records.
7. **Responsible Alert Generation:** Generate alerts with severity, reasons, recommended actions, and human-review status.

## 🔍 Key Features

### 1. Login Threat Detection
Uses a Decision Tree model to classify login activity into Normal and Suspicious categories.

### 2. Prediction Confidence
Calculates the maximum predicted class probability to indicate the model's confidence in each prediction.

### 3. Explainable AI
Displays feature importance through a labelled bar chart to help understand which inputs influence the model.

### 4. Sensitivity Analysis
Tests how changing the number of failed login attempts affects the model's prediction and confidence.

### 5. Privacy Protection
Masks sensitive identifiers:
- IP addresses: `192.168.10.24` → `192.168.xxx.xxx`
- Account IDs: `ACC-1001` → `ACC-1***01`

### 6. Responsible Security Alerts
Generates alerts containing:
- Severity level
- Reason for the alert
- Recommended security action
- Human-review requirement

## 🚨 Alert Severity Levels

| Severity | Condition | Recommended Action |
|---|---|---|
| High | Model predicts Suspicious | Verify, contain if required, and report |
| Medium | Non-suspicious prediction with confidence below 0.70 | Send for analyst review |
| Low | Normal prediction with sufficient confidence | Continue normal monitoring |

**Important:** High- and Medium-severity alerts require human review. The system does not automatically block accounts or punish users.

## 📂 Project Structure

```text
Explainable-Privacy-Aware-AI-Threat-Alert/
│
├── Lab_4_Explainable_Privacy_Aware_AI_Threat_Alert.ipynb
│
└── README.md
```

## 🚀 How to Run the Project

### Option 1: Google Colab

1. Download or clone this repository.
2. Open [Google Colab](https://colab.research.google.com/).
3. Upload the `.ipynb` notebook.
4. Run all cells sequentially.
5. Review the prediction tables, feature-importance chart, sensitivity results, masked records, and generated alerts.

### Option 2: Run Locally

**Step 1: Clone the repository**

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

**Step 2: Navigate to the project directory**

```bash
cd YOUR-REPOSITORY
```

**Step 3: Install dependencies**

```bash
pip install pandas matplotlib scikit-learn jupyter
```

**Step 4: Launch Jupyter Notebook**

```bash
jupyter notebook
```

**Step 5:** Open `Lab_4_Explainable_Privacy_Aware_AI_Threat_Alert.ipynb` and run all cells.

## 📈 Expected Outputs

After running the notebook, the following outputs are generated:

- Decision Tree model training confirmation.
- Baseline login prediction and confidence table.
- Lowest-confidence record.
- Feature-importance table and visualization.
- Before-and-after sensitivity analysis.
- Masked account IDs and IP addresses.
- Privacy and responsible-use rules.
- Final security alert table.
- Human-review recommendations.

## ⚠️ Limitations

- The project uses a small illustrative dataset.
- The Decision Tree model may not generalize to real-world cybersecurity environments.
- Prediction confidence does not guarantee prediction correctness.
- Feature importance does not establish causation.
- Real-world deployment requires larger, representative datasets and further validation.

This project is an educational prototype and should not be used as a standalone production security system.

## 🔐 Privacy and Responsible AI

The project follows these responsible-use principles:

- Mask sensitive identifiers before displaying or exporting data.
- Use sanitized data for experimentation.
- Restrict access to unmasked records.
- Require human review for high-risk alerts.
- Avoid automatic punishment or account blocking based solely on AI predictions.

## 🎓 Project Information

**Course:** ENSP355 – AI in Cyber Security  
**Lab:** Lab 4 – Explainable and Privacy-Aware AI Threat Alert  
**Programme:** B.Tech CSE (Core)  
**Platform:** Python / Google Colab

---

## 📜 License

This project is intended for educational and academic purposes. You may modify and extend it for learning and experimentation.
