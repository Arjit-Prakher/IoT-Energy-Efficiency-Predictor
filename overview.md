
***

## Step 1: Finalize Your Project Type and Models

First, decide on the **primary goal** for one of your chosen datasets. Since you have two datasets, pick the one that is most suitable for a clear problem statement.

* **Classification:** Use this if your target variable is a category.
    * **Problem Example:** Predicting if a customer will churn ('Yes' or 'No').
    * **Common Models:** **C5.0**, **CHAID**, **Logistic Regression**, **Neural Net**, **SVM**.
* **Regression:** Use this if your target variable is a continuous number.
    * **Problem Example:** Predicting the price of a house or the total sales amount.
    * **Common Models:** **Linear Regression**, **Neural Net**.
* **Clustering:** Use this if you don't have a target variable and want to find natural groups in your data.
    * **Problem Example:** Segmenting customers into different groups based on their purchasing behavior.
    * **Common Models:** **K-Means**, **TwoStep**, **Kohonen**.

Based on your team size, you will need to build the required number of models for this **single problem statement**. For example, a team of 2 will choose one dataset and one problem (e.g., classification) and build 3 different classification models to compare their performance.

***

## Step 2: The Actual Project in IBM SPSS Modeler (The Stream)

This is the core of your project. Your stream should tell a clear story from raw data to final evaluation. Take screenshots at every major step.



### A. Data Import and Exploration
1.  **Data Source Node:** Use a `Var. File` (for CSV) or `Excel` node to import your dataset onto the canvas.
2.  **Type Node:** This is the **most important** initial step. Connect the source node to a `Type` node.
    * **Check Measurement:** Ensure each field's measurement level is correct (Continuous, Nominal, Ordinal, Flag).
    * **Set Roles:** Define the role for each variable. You must set one field as the **Target** (the variable you are trying to predict). The others will be **Input**. Set irrelevant fields like ID columns to **None**.
3.  **Data Audit Node:** Connect a `Data Audit` node (from the Output palette) to your `Type` node. Run it to get a summary of your data, including histograms, statistics, and the number of missing values. **Take screenshots of this for your report.**

### B. Data Preparation
1.  **Partition Node:** For predictive modeling (Classification/Regression), you must split your data. Connect a `Partition` node and divide your data into a **Training set** (e.g., 70%) and a **Testing set** (e.g., 30%). The models will be built on the training data and validated on the unseen testing data.
2.  **Select / Filter / Derive Nodes (If Needed):**
    * Use a `Select` node if you need to work on a subset of your data (e.g., "select all customers from a specific country").
    * Use `Filter` to remove fields you don't need.
    * Use `Derive` to create new fields (e.g., `Age` from `Date of Birth`).

### C. Modeling
1.  **Connect Model Nodes:** Connect your chosen model nodes (e.g., `C5.0`, `Logistic Regression`, `CHAID`) to the `Partition` node. You can connect them all in parallel to the same `Partition` node.
2.  **Run the Models:** Run each modeling node. This will generate a **model nugget** (a golden diamond-shaped icon) for each model on your canvas. These nuggets contain the results.

### D. Evaluation
1.  **Connect Nuggets to Output Nodes:** Connect all your model nuggets to an **`Analysis`** node and a **`Table`** node. This will allow you to see and compare the performance of all your models at once.
2.  **Analyze Results:** Run the `Analysis` node. It will show you the accuracy of each model on your testing data. For classification, it will show a **confusion matrix**.
    * **For Classification**, the key metric is **Accuracy**.
    * **For Regression**, the key metric is **R-squared** or **Mean Absolute Error**.
3.  **Evaluation Chart:** Connect an **`Evaluation`** chart to the model nuggets to visually compare performance using charts like Gain or Lift charts. **Take screenshots of the `Analysis` output and any relevant charts.**

***

## Step 3: Structuring Your Project Report (Word/PDF)

Follow the required structure precisely. Use the screenshots you took while building the stream.

* **0. University Cover Page:** Your standard university title page.
* **1. Index:** A table of contents.
* **2. Summary of Project (Abstract):** A brief, high-level overview. In one paragraph, state the problem (e.g., "predicting customer churn"), the dataset used, the models built (e.g., "C5.0, CHAID, and Logistic Regression"), and the main finding (e.g., "The C5.0 model was the most accurate at 88%").
* **3. Project Introduction:**
    * **Problem Statement:** Describe the business problem you are solving.
    * **Dataset Description:** Explain your dataset. What do the rows and columns represent? What is the source? Include a small table showing the metadata (variable names, data types, descriptions).
    * **Objective:** Clearly state your goal, e.g., "The objective of this project is to build and evaluate three different classification models to predict employee attrition and identify the best-performing model."
* **4. Actual Project Details (with screenshots):** This is the longest section. Structure it based on your workflow.
    * **4.1 Data Exploration:** Show the screenshot of your `Data Audit` node's output. Discuss key findings like missing data or the distribution of important variables.
    * **4.2 Data Preparation:** Explain the steps you took. Show a screenshot of your `Type` node settings (especially the target variable). Explain why you used a `Partition` node.
    * **4.3 Modeling:**
        * Briefly introduce each model you used (e.g., "C5.0 is a decision tree algorithm...").
        * Show a screenshot of your complete SPSS stream.
        * For each model, show a screenshot of the model nugget's output (e.g., the decision tree for C5.0, the predictor importance chart).
    * **4.4 Model Evaluation & Comparison:**
        * Show the screenshot of the `Analysis` node output comparing all models.
        * Include a table that summarizes the key performance metric (e.g., Accuracy) for each model.
        * Declare the "winner." Which model performed best on the testing data?
* **5. Conclusion:**
    * **Summary of Findings:** Briefly reiterate which model was the best and why.
    * **Business Implications:** How could a business use your findings? (e.g., "By using the C5.0 model, the company can proactively identify customers at high risk of churning and target them with retention offers.")
    * **Limitations & Future Work:** Mention any limitations of your project and suggest how it could be improved in the future.

***

## Step 4: Creating the PowerPoint Presentation (PPT)

Keep it visual and to the point (10-12 slides max). The goal is to demo your work, not read theory.

* **Slide 1: Title Slide:** Project Title, Team Members.
* **Slide 2: Problem Statement & Objective:** What problem are you solving?
* **Slide 3: Dataset Overview:** Briefly describe the data.
* **Slide 4: The Workflow:** A single, large, clear screenshot of your final SPSS Modeler stream. Briefly explain the flow.
* **Slides 5-7 (1-2 slides per model): Model Results:**
    * Show a key visual from the model (e.g., the decision tree, a predictor importance chart).
    * State its accuracy.
* **Slide 8: Model Comparison:** The most important slide! A simple table or bar chart comparing the accuracy of all your models.
* **Slide 9: Best Model Deep Dive:** A closer look at your best-performing model.
* **Slide 10: Conclusion & Business Recommendation:** Summarize your findings and explain how your model can provide business value.
* **Slide 11: Live Demo (Optional but recommended):** If time permits, quickly show your actual SPSS stream and run the `Analysis` node to prove your results.
* **Slide 12: Q&A:** A simple "Thank You" or "Questions?" slide.

***

## Step 5: GitHub Submission

1.  Create a new public repository on GitHub.
2.  Create a clear folder structure:
    * `Project Report/` (for your PDF/Word file)
    * `Presentation/` (for your PPT file)
    * `SPSS Files/` (for your stream `.str` file)
3.  Write a simple `README.md` file in the main directory. Explain the project in a few sentences and describe the contents of each folder.
4.  Upload all your files into the correct folders.
5.  Share the link to your GitHub repository.