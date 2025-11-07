# 💡 Predictive Modeling of Energy Consumption in IoT Communication Networks

### Project Name: IoT-Energy-Efficiency-Predictor

## 📋 1. Project Overview

This project focuses on applying predictive analytics techniques to a dataset concerning **Energy-Efficient Communication Protocols for Large-Scale IoT Deployments**. The goal is to build machine learning models using **IBM SPSS Modeler** to forecast critical network performance metrics, specifically **energy consumption (Regression)** and **transmission reliability (Classification)**.

The project fulfills the requirements for the **Predictive Analysis** course, requiring the development and comparison of at least **three distinct predictive models** (for a team of 2).

### 🎯 Key Objectives

1.  **Regression:** Predict the **`energy_consumed`** (Joules) for a given data transmission based on factors like device, protocol, distance, and environment.
2.  **Classification:** Predict the binary outcome of **`transmission_success`** (Success/Failure) to identify reliable communication setups.
3.  **Clustering and Regression:** Segment data based on their behavior and applying Linear Regression and comparing values.

---

## 🛠️ 2. Tools & Dataset

| Component | Detail |
| :--- | :--- |
| **Primary Tool** | **IBM SPSS Modeler v18+** (Used for data preparation, modeling, and evaluation). |
| **Dataset** | **Energy-Efficient Communication Protocols** (Kaggle Source: [https://www.kaggle.com/datasets/tinutinu32/energy-efficient-communication-protocols]). |
| **Dataset Size** | **18 fields, 8738 records** |
| **Deliverables** | Project Report (PDF/Word), PowerPoint Presentation (PPT), SPSS Modeler Stream (`.str` file). |

---



## ⚙️ 4. Modeling Approach (The 3 Models)

The SPSS Modeler stream utilizes a 70/30 split for Training/Testing data to ensure robust model validation.

| Model # | Model Type | SPSS Node Used | Target Variable | 
| :--- | :--- | :--- | :--- 
| **1 (Classification)** | **Decision Tree** | C5.0 | `transmission_success`
| **2 (Regression)** | **Statistical Model** | Linear Regression | `energy_consumed` 
| **3 (Clustering)** | **TwoStep** | Linear Regression | `transmission_success` or `energy_consumed` 

---



## 👥 6. Team & Submission Details

| Role | Name | Student ID |
| :--- | :--- | :--- |
| Team Member 1 | **Stuti Kumari** | **AJU/241581** |
| Team Member 2 | **Arjit Prakher** | **AJU/241367** |

**Submission Date:** **13/10/2025**
