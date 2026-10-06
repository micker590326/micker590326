# Hi, I'm Fang-Yi Chen (Miki) 👋

I'm a recent graduate from Tamkang University (Management Sciences, 2022–2026), based in Taiwan. I like turning messy raw data into something that actually tells a story — cleaning it up, running the numbers, and figuring out what it means.

This page collects a few school projects where I did exactly that: survey data, a computer-vision experiment, a classification model, and a household carbon-tracking log. None of them were "real" industry work, but each one taught me something about data quality, statistics, or testing that I keep using.

📫 Reach me at mickey590326@gmail.com

---

## What I Work With

| Area | Tools / Methods | Application |
|---|---|---|
| Data Cleaning & Quality Checking | Excel, CSV | Cleaned 202 raw survey responses, handling missing values and invalid entries |
| Measurement Reliability Validation | SPSS (Cronbach's α) | Validated internal consistency across a 45-item scale (α = 0.68–0.90) |
| Statistical Analysis & Indicator Construction | SPSS (Factor Analysis, Regression, Chi-square) | Extracted quality dimensions from raw data and tested the significance of causal paths |
| Model Testing & Results Logging | Python, Google Colab | Executed YOLO object-detection model tests, logging accuracy and defect types |
| Basic Quality Control Tools | Excel Charts | Built check sheets, Pareto charts, and cause-and-effect diagrams (self-study) |

---

## Certificates

| Certificate | Link |
|---|---|
| Microsoft Office Specialist (MOS) Excel | [📄 View Certificate](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/Excel%E8%AD%89%E6%9B%B8.pdf) |
| Corporate Carbon Strategy and Sustainable Transformation — Completion Certificate | [📄 View Certificate](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/%E4%BC%81%E6%A5%AD%E7%A2%B3%E7%AD%96%E7%95%A5%E8%88%87%E6%B0%B8%E7%BA%8C%E8%BD%89%E5%9E%8B%20%E7%B5%90%E6%A5%AD%E8%AD%89%E6%98%8E.pdf) |

---

## Projects

---

### Project 1 | Quantitative Validation of Consumer Service Quality Indicators

**Course**: Research Methods, Dept. of Management Sciences (Junior Year)
**Date**: May 2025
**Role**: Questionnaire design, data collection, chi-square testing (individual contribution)

**What I did**

Designed a structured questionnaire (45 items across three constructs: Involvement, Satisfaction, Motivation) to study budget-airline service quality. Collected 202 responses via Google Forms, exported to CSV, and performed the following data-quality work:

- **Raw data cleaning**: Identified and flagged 37 valid missing-value cases among respondents who had skipped sections after indicating they had not flown with a budget airline, ensuring the correct subset was used for analysis
- **Measurement reliability validation (MSA-equivalent)**: SPSS Cronbach's α analysis — overall α = 0.772, construct-level α ranging 0.68–0.90; identified and removed item INV14 for low reliability
- **Construct validity confirmation**: KMO = 0.801 (Involvement construct), passed Bartlett's test of sphericity (p < 0.001), confirming suitability for factor analysis
- **Causal path verification**: Regression analysis confirmed a significant positive path from "usage motivation" to "satisfaction" (p < 0.05)
- **Subgroup comparison**: Chi-square test confirmed a significant difference in service perception by occupation (Pearson χ² = 49.056, p = 0.002)

**What this shows**

| Skill | How it shows up here |
|---|---|
| Data quality management | Identifying missing values, invalid responses, and skip-logic errors |
| Measurement reliability | Cronbach's α to confirm measurement consistency |
| Stratified analysis | Chi-square comparisons by occupation and age group |
| Indicator construction | Factor analysis to extract convenience, safety, and satisfaction dimensions |

**Tools**: SPSS, Excel (pivot tables on 202 records), Google Forms
**Deliverables**: Raw survey CSV + reliability summary table + regression coefficient table + chi-square results table

📁 **Files**: [Research Report (PDF)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/%E5%BB%89%E5%83%B9%E8%88%AA%E7%A9%BA%E7%A0%94%E7%A9%B6%E5%A0%B1%E5%91%8A.pdf) | [Raw Survey Data (CSV, 202 responses)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/%E5%BB%89%E5%83%B9%E8%88%AA%E7%A9%BA%E5%B8%82%E5%A0%B4%E8%AA%BF%E6%9F%A5%E5%95%8F%E5%8D%B7.csv) | [Pivot Analysis (Excel)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/pivot_202survey.xlsx)

---

### Project 2 | Object Detection Model Testing & Defect Analysis

**Course**: Introduction to Artificial Intelligence (Sophomore Year)
**Date**: April 2024
**Role**: Completed independently

**What I did**

Built a complete model-testing pipeline on a pretrained YOLOv4 model in Google Colab, simulating a data quality assurance (DQA) product-testing workflow:

- **Test environment setup**: Loaded `yolov4.weights` and verified GPU environment
- **Test case execution**: Ran detection on static test images (person, dog, motorcycle), logging bounding-box positions and confidence scores
- **Result verification**: Confirmed the distribution of True Positives, False Positives, and False Negatives
- **Defect classification**: Catalogued misclassification patterns in "small object," and "overlapping multi-object" scenarios, and analyzed root causes
- **Improvement recommendations**: Proposed 3 concrete improvements (data augmentation, multi-scale feature fusion, loss function refinement)

**What this shows**

| Skill | How it shows up here |
|---|---|
| Structured testing | Full cycle of defining test conditions → execution → logging results → defect analysis |
| Error classification | Categorizing misclassifications by scenario (small object / overlap / low resolution) |
| Root cause analysis | Explaining localization errors via grid-partitioning limitations |
| Technical reporting | Compiling test conditions, accuracy, defect list, and improvement recommendations |

**Tools**: Google Colaboratory, Python, YOLOv4
**Deliverables**: `model_test_log.md` (test versions, conditions, results, defect classification table)

📁 **Files**: [Midterm Report (PDF)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/YOLO%E4%BA%BA%E8%87%89%E8%BE%A8%E8%AD%98%E6%9C%9F%E4%B8%AD%E5%A0%B1%E5%91%8A.pdf) | [YOLO Test Log](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/yolo_test_log.md) | [Pareto Defect Analysis (Excel)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/pareto_defect_chart.xlsx)

---

### Project 3 | Classification Model Building, Code Book Design & Accuracy Validation

**Course**: Data Mining (Junior Year)
**Date**: Fall 2025
**Role**: Team project (responsible for Code Book design and decision-tree validation)

**What I did**

Built a decision-tree classification model and designed a complete Code Book as a data dictionary (equivalent to a QA specification document):

- **Code Book creation**: Defined the name, data type, value range, and encoding rules for each variable to ensure consistent data entry
- **Data validation**: Verified that each field complied with the Code Book specification (range checks, type checks)
- **Model testing**: Validated classification accuracy using a train/test split, logging error rates for each branch
- **Error logging**: Compiled misclassified cases and analyzed which sample types were most error-prone

**What this shows**

| Skill | How it shows up here |
|---|---|
| Specification design | Code Book as a data dictionary defining valid/invalid conditions |
| Input validation | Type and range checks on input data |
| Model evaluation | Recording classification accuracy and error rates by branch |

**Tools**: Python (sklearn), Excel (Code Book management)
**Deliverables**: Code Book variable definition table + decision-tree model evaluation table

📁 **Files**: [Final Report (PDF)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/CodeBook%E6%B1%BA%E7%AD%96%E6%A8%B9%E6%9C%9F%E6%9C%AB%E5%A0%B1%E5%91%8A.pdf) | [Stress Level Dataset (CSV)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/stress_level_dataset.csv)

---

### Project 4 | Household Energy Carbon Emissions Data Collection & Quality Review

**Course**: Environmental Management Seminar (Senior Year)
**Date**: Fall 2025

**What I did**

Built a household carbon-emissions inventory system, designing a data-collection form and performing data-quality validation:

- **Structured form design**: Created standardized recording fields for electricity, natural gas, and transportation categories
- **Value quality review**: Cross-checked calculated values against official emission factors (Taiwan Bureau of Energy) to verify reasonableness
- **Outlier detection**: Flagged months with values deviating more than 2σ from the historical mean and traced back to the original records
- **Report compilation**: Produced category-level emission totals and monthly trends via pivot tables

**What this shows**

| Skill | How it shows up here |
|---|---|
| Data validation | Reviewing input data against reference coefficients |
| Outlier detection | 2σ deviation flagging triggering a data-trace workflow |
| Record keeping | Traceable monthly, categorized collection records |
| Reporting | Pivot-table summaries formatted for easy review |

**Tools**: Excel (SUMIF, pivot tables, conditional formatting)
**Deliverables**: Monthly carbon emissions record (with outlier flags) + monthly trend pivot table

📁 **Files**: [Final Report (PDF)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/%E7%A2%B3%E7%9B%A4%E6%9F%A5%E6%9C%9F%E6%9C%AB%E5%A0%B1%E5%91%8A.pdf) | [Carbon Emissions Record (Excel)](https://github.com/micker590326/QA-Internship-Portfolio/blob/main/carbon_record_template.xlsx)

---

## About Me

**Education**: B.A. in Management Sciences, Tamkang University (2022–2026)

**Analytical & Data Quality Foundations**
- Familiar with the PDCA cycle and quality-improvement processes
- Familiar with the seven basic QC tools (check sheets, Pareto charts, cause-and-effect diagrams, scatter diagrams, control charts, histograms, stratification)
- Understand the basics of Measurement System Analysis (MSA): repeatability and reproducibility
- Experienced in data consistency validation: range checks, type checks, missing-value handling
- Familiar with the basics of Statistical Process Control (SPC)

**Personal Traits**
- Systematic planner (currently executing a structured IELTS preparation plan)
- Habit of documenting every step for traceability
- Fast learner of new tools; comfortable solving problems independently from documentation

---

*Last updated: October 2026*
