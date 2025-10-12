# 💡 Predictive Modeling of Energy Consumption in IoT Communication Networks

### Project Name: IoT-Energy-Efficiency-Predictor

## 📋 1. Project Overview

This project focuses on applying predictive analytics techniques to a dataset concerning **Energy-Efficient Communication Protocols for Large-Scale IoT Deployments**. The goal is to build machine learning models using **IBM SPSS Modeler** to forecast critical network performance metrics, specifically **energy consumption (Regression)** and **transmission reliability (Classification)**.

The project fulfills the requirements for the **Predictive Analysis** course, requiring the development and comparison of at least **three distinct predictive models** (for a team of 2).

### 🎯 Key Objectives

1.  **Regression:** Predict the **`energy_consumed`** (Joules) for a given data transmission based on factors like device, protocol, distance, and environment.
2.  **Classification:** Predict the binary outcome of **`transmission_success`** (Success/Failure) to identify reliable communication setups.
3.  **Model Comparison:** Evaluate and compare the performance of three different algorithms to determine the "best" model for deployment.

---

## 🛠️ 2. Tools & Dataset

| Component | Detail |
| :--- | :--- |
| **Primary Tool** | **IBM SPSS Modeler v18+** (Used for data preparation, modeling, and evaluation). |
| **Dataset** | **Energy-Efficient Communication Protocols** (Kaggle Source: [Link to your specific Kaggle dataset page]). |
| **Dataset Size** | [**[Insert approximate row/column count here, e.g., 10,000 records, 17 fields]**] |
| **Deliverables** | Project Report (PDF/Word), PowerPoint Presentation (PPT), SPSS Modeler Stream (`.str` file). |

---

## 💻 3. Repository Contents

| File/Folder | Description | Corresponding Deliverable |
| :--- | :--- | :--- |
| `Report/` | Contains the complete project report file. | **Project File (Report)** |
| `Presentation/` | Contains the summary presentation slides (10-12 slides). | **PowerPoint Presentation** |
| `SPSS_Stream/` | Contains the core working file for the project. | **IBM SPSS Stream (`.str`)** |
| `data/` | Original and/or prepared dataset files. | **Dataset (CSV/TXT)** |
| `README.md` | This file, providing an overview and guide. | N/A |

---

## ⚙️ 4. Modeling Approach (The 3 Models)

The SPSS Modeler stream utilizes a 70/30 split for Training/Testing data to ensure robust model validation.

| Model # | Model Type | SPSS Node Used | Target Variable | Primary Evaluation Metric |
| :--- | :--- | :--- | :--- | :--- |
| **1 (Classification)** | **Decision Tree** | C5.0 | `transmission_success` | Accuracy & Confusion Matrix |
| **2 (Regression)** | **Statistical Model** | Linear Regression | `energy_consumed` | R-Squared and Residual Analysis |
| **3 (Hybrid)** | **Non-Linear Model** | Neural Network (ANN) | `transmission_success` or `energy_consumed` | ROC/Gains Chart (Classification) or R-Squared (Regression) |

---

## 📈 5. Key Findings (To be updated after analysis)

* **Best Performing Model:** [**[Insert Best Model Name Here]**] achieved the highest [**[Insert Metric, e.g., Accuracy / R-Squared]**] of **[**[Insert Value]**]% / **[**[Insert Value]**]**.
* **Key Predictors for Energy:** The most significant factors influencing energy consumption were identified as **[**[e.g., `protocol`, `distance`, `data_size`]**]**.
* **Optimal Communication:** The models suggest that the **[**[e.g., LoRa / NB-IoT]**]** protocol offers the best combination of low energy consumption and high transmission success under typical deployment conditions.

---

## 👥 6. Team & Submission Details

| Role | Name | Student ID |
| :--- | :--- | :--- |
| Team Member 1 | **Stuti Kumari** | **[Your Student ID]** |
| Team Member 2 | **Arjit Prakher** | **[Partner's Student ID]** |

**Submission Date:** **13/10/2025**