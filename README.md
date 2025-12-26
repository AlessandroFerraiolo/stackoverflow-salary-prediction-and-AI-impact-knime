# 💰 Benchmarking Developer Compensation in the Age of AI
### 📊 Big Data & Databases Project | Bocconi University

## 🏫 About The Project
This repository contains the final group project for the **Big Data & Databases** course at **Bocconi University**.

Using the **2025 Stack Overflow Developer Survey** (approx. 49,000 respondents), we built an end-to-end data science pipeline in **KNIME** to benchmark global software developer salaries. The goal was to act as a "software company" reassessing compensation strategies to understand if the productivity claims of AI adoption justify higher salary offers.

## 🧠 Key Insight: The "AI-Confidence" Red Flag
One of our most critical findings challenges the common narrative that AI mastery currently commands a massive salary premium. We observed a trend consistent with the **Dunning-Kruger effect**:

> **🚩 The "AI Complex" Paradox**
> Developers who claimed that AI tools handle *complex* tasks "Very Well" earned, on average, **18–19% less** than their peers.

**Why?**
Our analysis suggests that less experienced (junior) developers—who naturally command lower salaries—tend to overestimate AI's capabilities for complex architecture. In contrast, high-earning senior engineers are more skeptical, likely because they work on legacy systems or highly specific architectures where current AI tools struggle.

**Managerial Implication:**
If a candidate demands a salary raise solely based on their belief that "AI can handle all complex tasks," it may actually signal **lower seniority** rather than elite productivity. Confidence in AI for complex work correlates with *lower* market value, making it a potential "red flag" during negotiation rather than a green light for a premium.

## 🔍 Other Findings
* **Geography is King:** Location remains the #1 driver of salary. For example, Western Europe offers salaries ~37% lower than the North American baseline.
* **Experience vs. Age:** "Years of Coding" helps predicts salary better than biological age. The growth curve peaks around 29–30 years of experience.
* **Remote Premium:** Fully remote roles showed an approximate **+9% salary premium** over in-person roles, likely due to access to global (higher-paying) labor markets.

## 🛠️ The Workflow (KNIME)
The project is implemented as a complete KNIME workflow covering:
1.  **Data Cleaning:** Handling missing values and filtering outliers.
2.  **Feature Engineering:**
    * **Consolidation:** Grouping 150+ countries into UN Macro-Regions.
    * **Text Processing:** Transforming multi-select fields (e.g., "Languages Used") into binary features.
    * **Custom Metrics:** Creating binary indicators for "Active AI Users".
3.  **Modeling & Evaluation:**
    We trained and compared 5 models. **Gradient Boosting (XGBoost)** was the best performer, explaining **~63%** of the variance in the test set.

| Model | Test R² | Insight |
| :--- | :--- | :--- |
| **Linear Regression** | 0.511 | Baseline performance |
| **Polynomial Regression** | 0.539 | Captured quadratic relationship of Age/Experience |
| **Random Forest** | 0.546 | Good generalization  |
| **Multilayer Perceptron** | 0.536 | Neural Net with RProp  |
| **Gradient Boosting** | **0.626** | **Best Performance**  |

## 📂 Repository Structure
* `workflow/`: The `.knwf` files to run the analysis.
* `presentation/`: The project slides (`report big data.pptx`) detailing the business case.

## 🚀 Usage
1.  Clone this repo.
2.  Import the `.knwf` file into **KNIME Analytics Platform**.
3.  Execute the workflow to reproduce the cleaning, modeling, and scoring steps.
OR
access at https://hub.knime.com/s/EMExIeg2lR1PnepV thorugh KNIME community hub
