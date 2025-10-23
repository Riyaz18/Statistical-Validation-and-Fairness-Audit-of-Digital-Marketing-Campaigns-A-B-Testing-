# Statistical Validation and Fairness Audit of Digital Marketing Campaigns (A/B Testing)

A data science solution that implements a rigorous **A/B Testing** framework to statistically validate the performance and algorithmic fairness of personalized versus standard marketing campaigns.

---

## Project Title & Short Description

**Title:** Statistical Validation and Fairness Audit of Digital Marketing Campaigns (A/B Testing)

**Description:** This project constructs an **A/B Testing** pipeline to compare the effectiveness of a **Standard Email Campaign (Group A)** against a **Personalized Email Campaign (Group B)**. The analysis focuses on key metrics (Open Rate, CTR) and essential fairness indicators (Disparate Impact based on Gender).

---

## Problem Statement / Goal

The primary goal is to provide a **statistically significant and ethically sound recommendation** for scaling up a new marketing strategy. This involves:
1.  **Quantifying Performance**: Determining if the personalized approach (B) leads to a statistically significant lift in core engagement metrics (Open Rate, Click-Through Rate) compared to the control (A).
2.  **Algorithmic Fairness**: Auditing the campaign for **Disparate Impact (DI)** to ensure that the new strategy does not unintentionally disadvantage any protected demographic group (e.g., based on `gender`).

---

## Tech Stack / Tools Used

The project is implemented in Python and utilizes statistical and data handling libraries critical for experimental design and validation:

| Category | Tool / Library | Purpose |
| :--- | :--- | :--- |
| **Data Handling** | Pandas NumPy | Data loading cleaning and numerical operations |
| **Statistics** | SciPy Statsmodels | Performing statistical significance tests (p-values) |
| **Visualization**| Matplotlib Seaborn | Generating comparative visualizations (Bar Plots) for results |
| **Testing** | Custom Functions | Calculating Disparate Impact and performing two-sample Z-tests |

---

## Approach / Methodology

1.  **Data Generation**: Generated a synthetic dataset simulating customer responses to two different email campaigns (Group A and Group B).
2.  **Metric Calculation**: Calculated the primary performance indicators for each group: **Open Rate** and **Click-Through Rate (CTR)**.
3.  **Statistical Validation**: Performed **Two-Sample Z-Tests** (implied in the p-value calculation) on the key metrics to determine the statistical significance of the observed difference between Group A and Group B.
4.  **Fairness Audit**: Calculated the **Disparate Impact (DI)** metric, which compares the ratio of the positive outcome (e.g., click rate) between an unprivileged group and a privileged group.
5.  **Reporting and Visualization**: Compiled the final metrics and used **Seaborn** to create a clear visual comparison of the results for stakeholder reporting.

---

## Results / Key Findings

The A/B test provided clear evidence supporting the deployment of the personalized campaign:

| Metric | Standard (A) | Personalized (B) | p-value | Interpretation |
| :--- | :--- | :--- | :--- | :--- |
| **Open Rate** | 24.3% | 27.5% | **< 0.0001** | **B is Significantly Better** |
| **Click-Through Rate**| 12.8% | 14.1% | 0.052 | **Borderline Significant** |

* **Performance**: The Personalized Campaign (B) showed a **statistically significant increase in Open Rate** and a near-significant increase in CTR.
* **Fairness**: The Fairness Audit showed that Group A had a DI ≈ 0.90 (slight disadvantage for the unprivileged group), while Group B had a DI ≈ 1.08, indicating the **Personalized Campaign (B) improves engagement without introducing gender bias**.

---

## Topic Tags

ABTesting MarketingCampaigns StatisticalValidation BusinessIntelligence DataScience AlgorithmicFairness DisparateImpact Python Pandas

---

## How to Run the Project

### 1. Install Requirements

Install all necessary packages using the provided `requirements.txt` file:

```bash
pip install -r requirements.txt
