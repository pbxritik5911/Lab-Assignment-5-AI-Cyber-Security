# Mini AI Cybersecurity Assistant

## 🔐 Project Overview

The **Mini AI Cybersecurity Assistant** is an integrated AI-based cybersecurity prototype developed using Python and Google Colab.

The project combines rule-based threat detection, Machine Learning, Deep Learning, Explainable AI (XAI), and privacy-aware security practices to identify potentially suspicious messages and login activities.

The assistant analyzes sample messages for phishing, malware, and ransomware indicators while simultaneously evaluating login behavior using a Decision Tree and a small Neural Network.

It generates an integrated security assessment by comparing model predictions, explaining suspicious activities, masking sensitive information, assigning risk levels, and recommending safe actions with human verification.

## 🎯 Project Objectives

- Recognize common cybersecurity threats using AI.
- Clean and anonymize message and login-activity data.
- Implement a rule-based threat detection system.
- Use a Decision Tree for suspicious login detection.
- Implement a small Neural Network and compare its predictions.
- Explain predictions using keywords, feature importance, and numerical reasons.
- Apply privacy protection and risk assessment.
- Generate responsible security alerts.
- Include human review for high-risk, conflicting, or low-confidence predictions.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Google Colab | Development environment |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Scikit-learn | Decision Tree and preprocessing |
| TensorFlow / Keras | Neural Network implementation |
| Matplotlib | Data visualization |
| Machine Learning | Login threat classification |
| Explainable AI | Prediction interpretation |

## 🏗️ System Architecture

The project consists of six major stages:

1. **Input and Privacy Module**
   - Accepts a sample message and login activity.
   - Cleans input data.
   - Masks sensitive identifiers such as email addresses, IP addresses, and account IDs.

2. **Rule-Based Threat Detection**
   - Checks messages for suspicious keywords.
   - Identifies phishing, malware, and ransomware indicators.
   - Generates matched keywords and a threat score.

3. **Decision Tree Classifier**
   - Analyzes numerical login activity.
   - Predicts Normal or Suspicious behavior.
   - Calculates prediction confidence.

4. **Neural Network**
   - Processes scaled numerical login features.
   - Predicts Normal or Suspicious activity.
   - Generates a prediction probability.

5. **Explainability Module**
   - Displays matched threat keywords.
   - Identifies important login features.
   - Provides numerical and threshold-based explanations.

6. **Risk and Response Module**
   - Combines outputs from all detection modules.
   - Assigns Low, Medium, or High risk.
   - Recommends safe actions.
   - Requests human review when necessary.

## 📊 Login Activity Features

The numerical login record contains four features:

| Feature | Description |
|---|---|
| `failed_logins` | Number of unsuccessful login attempts |
| `login_hour` | Hour of login activity |
| `new_device` | Indicates whether a new device is being used |
| `download_mb` | Amount of data downloaded in MB |

The machine-learning and deep-learning modules use these features to identify potentially suspicious login behavior.

## 🔍 Key Features

### 1. Rule-Based Threat Detection

Analyzes messages using predefined suspicious keywords and identifies possible:

- Phishing attacks
- Malware indicators
- Ransomware indicators

The module returns a threat category, matched keywords, and keyword-based score.

### 2. Machine Learning – Decision Tree

Uses a Decision Tree classifier to analyze login activity and classify it into:

- Normal
- Suspicious

The model also provides prediction confidence and feature importance.

### 3. Deep Learning – Neural Network

Implements a small pre-designed Neural Network using TensorFlow/Keras.

- Uses scaled numerical features.
- Produces prediction probabilities.
- Classifies login activity using a probability threshold of 0.50.

### 4. Model Comparison

Compares the outputs of three detection approaches:

- Rule-Based Detector
- Decision Tree Classifier
- Neural Network

The results are displayed together to provide an integrated security assessment.

### 5. Explainable AI (XAI)

Provides understandable reasons behind predictions through:

- Matched suspicious keywords.
- Feature importance.
- Threshold-based explanations.
- Numerical login activity analysis.

### 6. Privacy Protection

Protects sensitive information by masking:

- Email addresses
- IP addresses
- Account IDs

Only synthetic or sanitized data should be used.

### 7. Risk Assessment and Security Alerts

Assigns one of three risk categories:

| Risk Level | Interpretation |
|---|---|
| Low | Activity appears normal |
| Medium | Potential threat or uncertain prediction |
| High | Strong indication of suspicious activity |

### 8. Human-in-the-Loop Security

Human review is required when:

- The risk level is High.
- Different detection models produce conflicting results.
- Prediction confidence is low.

The system provides decision support rather than automatically taking punitive security actions.

## 🔄 Integrated Workflow

```text
       Sample Message + Login Activity
                     |
                     v
             Input & Privacy
                     |
                     v
             Data Cleaning
                     |
          +----------+----------+
          |          |          |
          v          v          v
       Rule-Based  Decision   Neural
       Detection    Tree     Network
          |          |          |
          +----------+----------+
                     |
                     v
             Model Comparison
                     |
                     v
              Explainability
                     |
                     v
              Risk Assessment
                     |
                     v
              Safe Action
                     |
                     v
               Human Review
                     |
                     v
              Final AI Alert
```

## 🧪 Demonstration Scenarios

The project is designed to test five scenarios:

| Scenario | Test Case | Expected Interpretation |
|---|---|---|
| 1 | Normal message and normal login | Low risk; human review usually not required |
| 2 | Urgent account-verification message | Phishing indicator; Medium/High risk |
| 3 | Repeated failed logins on a new device | Suspicious numeric result; High risk |
| 4 | Large download at an unusual time | Alert with numerical explanation |
| 5 | Conflicting or low-confidence predictions | Human review required |

## 📈 Expected Outputs

After executing the notebook, the project should generate:

- Threat category and matched keyword results.
- Decision Tree predictions and confidence.
- Neural Network predictions and probabilities.
- Combined model comparison table.
- Feature-importance visualization.
- Risk/category chart.
- Masked message and login information.
- Final integrated security alert.
- Recommended safe actions.
- Human-review status.

## 📂 Project Structure

```text
Mini-AI-Cybersecurity-Assistant/
│
├── Mini_AI_Cybersecurity_Assistant.ipynb
│
├── datasets/
│   ├── messages.csv
│   └── login_activity.csv
│
├── outputs/
│   ├── combined_results.csv
│   ├── risk_category_chart.png
│   └── feature_importance.png
│
├── screenshots/
│
└── README.md
```

*Note: The folder and filenames above are a suggested repository structure. Use the actual filenames generated by your notebook.*

## 🚀 How to Run the Project

### Option 1: Google Colab

1. Clone or download this GitHub repository.
2. Open [Google Colab](https://colab.research.google.com/).
3. Upload the project notebook.
4. Upload the required CSV datasets.
5. Execute all notebook cells sequentially.
6. Test all five demonstration scenarios.
7. Review the final prediction table, charts, and security alerts.

### Option 2: Run Locally

**Step 1: Clone the repository**

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

**Step 2: Navigate to the project**

```bash
cd YOUR-REPOSITORY
```

**Step 3: Install dependencies**

```bash
pip install pandas numpy matplotlib scikit-learn tensorflow jupyter
```

**Step 4: Launch Jupyter Notebook**

```bash
jupyter notebook
```

**Step 5:** Open the notebook and execute all cells.

## 📋 Project Deliverables

The capstone assignment includes the following deliverables:

- Completed and executed Google Colab notebook.
- Two supplied CSV datasets.
- One final combined result table.
- Risk/category chart.
- Feature-importance chart.
- Results for all five demonstration scenarios.
- Two-to-three-page project report.
- Five-slide presentation.
- One-page responsible-use and human-review checklist.
- Individual contribution statement for team submissions.

## ⚠️ Limitations

- The prototype is designed for educational purposes.
- Model performance depends on the quality and quantity of training data.
- Prediction confidence does not guarantee correctness.
- Rule-based detection may generate false positives.
- Neural Network and Decision Tree predictions may disagree.
- The prototype is not intended to replace professional cybersecurity monitoring systems.

## 🔒 Privacy and Responsible AI

This project follows responsible cybersecurity practices:

- Use only supplied synthetic or sanitized datasets.
- Do not upload institutional confidential data to Google Colab.
- Mask sensitive identifiers in screenshots, charts, and exported files.
- Do not open suspicious links or execute malware.
- Do not scan networks or test live accounts.
- Treat model predictions as decision-support information.
- Require authorized human verification before serious security actions.

## 🎓 Academic Information

**Course:** ENSP355 – AI in Cyber Security  
**Project:** Capstone – Mini AI Cybersecurity Assistant  
**Academic Year:** 2026–27  
**Platform:** Google Colab / Python  
**University:** K.R. Mangalam University  
**School:** School of Engineering & Technology

## 📜 License

This project is intended for educational and academic purposes. It may be modified and extended for learning, research, and experimentation.
