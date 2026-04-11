---
layout: page
title: Project 3
description: >-
    Reproduction or Open Data Project.
nav_order: 7
---

# Final Project Objectives

## Table of Contents

* [Project Tracks](#project-tracks)
* [Use of AI and Code Standards](#use-of-ai-and-code-standards)
* [Timeline & Milestones](#timeline--milestones)
* [Deliverables and Submissions](#deliverables-and-submissions)
    * [Checkpoint 1](#checkpoint-1)
    * [Checkpoint 2](#checkpoint-2)
    * [Final Submission](#final-submission)
* [Report Requirements](#report-requirements)
* [Enrollment and Topic Selection](#enrollment-and-topic-selection)
* [Track A: Starter Topics](#track-a-starter-topics)
* [Track B: Paper Reproduction](#track-b-paper-reproduction)
    * [The Task](#the-task)
    * [Approved Paper List](#approved-paper-list)
    * [Accessing Replication Archives](#accessing-replication-archives)

---

For your final project, your group will select one of two tracks. Both tracks are weighted equally and graded on the same rubric: clarity of question, quality of code, and quality of deliverables.

## Project Tracks

| Feature | Track A: Open Data Project | Track B: Paper Reproduction |
| :--- | :--- | :--- |
| **Focus** | Design and execute an original empirical project using public data. | Duplicate the results of a prior study using the same data and procedures. |
| **Requirements** | Pose a clear economic question and include an econometric baseline vs. ML comparison. | Re-code the analysis in your own environment (computational reproducibility). |
| **Deliverable** | An original analysis with a discussion on what worked and what didn't. | Regression tables and figures presented alongside the original paper's results. |

---

## Use of AI and Code Standards

You may use AI assistants (Claude, ChatGPT, Copilot, etc.) for this project. However, all AI-assisted code must meet the following strictly enforced standards:

* **Modular Code:** No function may be longer than 10 lines of code.
* **Professionalism:** No emojis anywhere in code, comments, or notebook text.
* **Documentation:** Every code cell *must* be preceded by a markdown cell explaining the "what" and "why."
* **Reproducibility:** The notebook must run start-to-finish with no manual intervention ("Run All").
* **Data Handling:** Any data not pulled from a public API at runtime must be included in your submission `.zip` file with a clear file path.
* **Disclosure:** Briefly disclose AI use in an appendix (tools used, tasks performed, and verification methods). Include any `agent.md` or `skill.md` files used.

---

## Timeline & Milestones

> **Note:** Late submissions are not accepted at any stage. After group sign-up closes, discussion sections become optional office hours.

* **April 15:** Group sign-up closes (Groups of 3–5).
* **April 17:** Finalized topic selection.
* **April 24:** Checkpoint 1 Due. (Short PDF: roles, track, topic, and repository screenshots).
* **May 1:** Checkpoint 2 Due. (Google Form: report on at least 3 successful/attempted results).
* **May 6:** Final Project Due.
* **May 8:** Peer Review Due.

---

## Deliverables and Submissions

### Checkpoint 1
**Due Date:** Friday, April 18, 2025

This will be a separate Gradescope assignment that will be due earlier. There is no need to submit any code; a write-up of your progress so far (preferably in LaTeX) will suffice.

**Submission Guidelines:**
* Everything must be submitted in a **single PDF**.
* Only the **group representative** should submit.
* **Important:** Include all group members in the Gradescope submission.

**Required Contents:**
* **Group Composition:** Names and assigned responsibilities.
* **Chosen Paper:** Citation/Title of the selected paper.
* **Project Organization:** Screenshots of the code organization (including any relevant data, notebooks, or scripts).
* **LaTeX Setup:** Screenshots of the LaTeX project in Overleaf following the **I4R template**.
* **Progress Report:** A description of what you have attempted to do so far.
* **Status Summary:** A summary of what is going well and what you are struggling with.
* **Staff Support:** A note on how course staff may help you succeed.

---

### Checkpoint 2
**Due Date:** Friday, April 25, 2025

One person from your group must fill out the designated **Google Form** for this checkpoint. 

* **Requirement:** While the form provides space to discuss up to 5 results, you are only required to discuss **3**.

---

### Final Submission

Final submission for **both** tracks consists of three components:

1.  **The Report:** 10–15 pages including graphs and tables.
    * **Track A:** Submit as `.md` or `.tex` AND a PDF.
    * **Track B:** Submit as `.tex` AND a PDF.
2.  **Analysis Notebook:** A PDF export of your Jupyter Notebook(s) submitted to Gradescope.
3.  **Reproducibility Link:** A zip file with runnable notebook with organized data subfolders.
4.  **Peer Evaluation:** A Google Form regarding group performance.

---

## Report Requirements

| Feature | Track A: Open Data | Track B: Paper Reproduction |
| :--- | :--- | :--- |
| **Introduction** | Define a specific policy/business challenge and its significance. | Summarize the original paper’s contribution and causal mechanism. |
| **Data** | Detail source (APIs, scraping), cleaning methods, and summary stats. | Detail access to original data vs. your own. Provide summary stats. |
| **Model** | Justify method choice. Show the logic and variable selection. | State the original model and exact equations authors used. |
| **Results** | Trends, regression tables, and coefficient explanations. | Replicate original graphs/tables as closely as possible. |
| **Discussion** | Data hurdles and limitations that could skew findings. | Reproduction hurdles and whether full replication was achieved. |
| **AI Usage** | Document help with code optimization or data cleaning. | Document help with code translation or LaTeX formatting. |

---

## Enrollment and Topic Selection

* **Starter Lists:** Track A topics and Track B papers are posted on Ed. You may propose your own by Checkpoint 1.
* **Enrollment Cap:** A maximum of **15 groups** may sign up for any single topic. Topics close once they reach this limit.
* **Peer Review:** Groups will exchange submissions via email. Group leaders must submit a review form verifying if the code runs and evaluating the quality of the work.

---

# Track A: Starter Topics

Each topic below is a starting point, not a script—your group is expected to refine the question, justify your data choices, and make real modeling decisions. All projects must include both an **econometric baseline** and a **machine learning comparison**, and must satisfy the code standards in the main spec.

> [!IMPORTANT]
> **Enrollment Cap:** A maximum of **15 groups** may sign up for each topic. Sign-ups are first-come, first-served via the sign-up sheet. Once a topic hits 15 groups, it closes; you must pick another or move to Track B (Reproductions).

---

### 1. Sovereign Credit Rating Reproduction
Build a model that predicts S&P or Moody's sovereign credit ratings from publicly available macro indicators, following the spirit of Cantor and Packer (1996). 

* **Data Sources:** Pull country-level data from World Bank WDI and IMF WEO (GDP per capita, growth, inflation, external debt, fiscal balance, default history). Scrape current ratings from Wikipedia.
* **Baseline:** Ordered logit or probit. 
* **ML Comparison:** Ordinal random forest or gradient boosting. 

---

### 2. GDP Nowcasting from Mixed-Frequency Indicators
Nowcast current-quarter US real GDP growth using monthly and weekly indicators released before the BEA advance estimate. 

* **Data Sources:** Pull data from FRED via `fredapi`: industrial production, retail sales, nonfarm payrolls, ISM, initial claims, etc. 
* **Target:** BEA quarterly GDP. 
* **Baseline:** Bridge equation or simple monthly-to-quarterly aggregation with OLS. 
* **ML Comparison:** Dynamic factor model or a simple recurrent network. 

---

### 3. State Unemployment Insurance Claims Forecasting
Forecast weekly initial unemployment insurance claims for three to five US states using FRED's state-level claims series.

* **Data Sources:** `CAICLAIMS`, `TXICLAIMS`, etc., via `fredapi`. Augment with state-level Google Trends data (via `pytrends`).
* **Baseline:** ARIMA or OLS with lagged claims and seasonal dummies. 
* **ML Comparison:** Gradient boosting (XGBoost/LightGBM) or a small LSTM. 

---

### 4. Intergenerational Mobility Across US Counties
Use the Opportunity Insights county-level mobility data to predict upward mobility from county characteristics.

* **Variables:** Segregation, school quality, family structure, income inequality, and commuting patterns. 
* **Baseline:** OLS using the variables emphasized by Chetty et al. 
* **ML Comparison:** Random forest with feature importance analysis. 

---

### 5. Election Forecasting from Economic Fundamentals
Replicate and extend a fundamentals-based presidential election model (e.g., Abramowitz's "Time for Change" or the Fair model).

* **Data Sources:** FRED (growth, inflation, unemployment) and presidential approval from Gallup or 538. Use county-level voting data for explanatory variables.
* **Baseline:** OLS (original specification). 
* **ML Comparison:** Regularized regression (Lasso or Ridge) given the small sample size.

---

### 6. Local Housing Price Nowcasting
Nowcast monthly housing price changes for a chosen metro area.

* **Data Sources:** Zillow ZHVI (Target) and a mix of FRED macro series, Census ACS demographics, and mortgage rate data (Features). 
* **Baseline:** OLS or ARIMA. 
* **ML Comparison:** Gradient boosting or a small neural network. 

---

# Track B: Paper Reproduction

For Track B, your group will attempt to replicate the results from a high-impact economics paper using Python. Each of the papers listed below received a **2025 or 2026 Best Paper Award** from the *American Economic Journal (AEJ)*.

## The Task

Your objective is to reproduce the analysis using Python and the data science tools introduced in this course. 

* **Code Originality:** While you may reference the original replication archives (often in Stata or R), the Python code you submit must be your own work.
* **Environment:** The analysis must be fully functional within a Google Colab environment.
* **Data Restrictions:** While most papers include full replication archives, some may have restricted data due to privacy. You must identify these limitations early. 

---

## Approved Paper List

### Applied Economics
* **Do Carbon Offsets Offset Carbon?**
    * *Journal:* AEJ: Applied Economics, Vol. 17, No. 1 (January 2025)
* **Working Remotely? Selection, Treatment, and the Market for Remote Work**
    * *Journal:* AEJ: Applied Economics, Vol. 16, No. 4 (October 2024)

### Economic Policy
* **Employed in a SNAP? The Impact of Work Requirements on Program Participation and Labor Supply**
    * *Journal:* AEJ: Economic Policy, Vol. 15, No. 1 (February 2023)
* **Adaptation and Adverse Selection in Markets for Natural Disaster Insurance**
    * *Journal:* AEJ: Economic Policy, Vol. 14, No. 3 (August 2022)

### Macroeconomics
* **Optimal Fiscal and Monetary Policy with Distorting Taxes**
    * *Journal:* AEJ: Macroeconomics, Vol. 17, No. 2 (April 2025)
* **Earnings-Based Borrowing Constraints and Macroeconomic Fluctuations**
    * *Journal:* AEJ: Macroeconomics, Vol. 15, No. 2 (April 2023)

### Microeconomics
* **The Fake News Effect: Experimentally Identifying Motivated Reasoning Using Trust in News**
    * *Journal:* AEJ: Microeconomics, Vol. 16, No. 2 (May 2024)
* **Competition in Pricing Algorithms**
    * *Journal:* AEJ: Microeconomics, Vol. 15, No. 2 (May 2023)

---

## Accessing Replication Archives
You can find the papers and their complete replication archives through the [American Economic Association (AEA) website](https://www.aeaweb.org/journals/aej). Ensure you download the "Replication Package" associated with your chosen paper to access the original data and source code.