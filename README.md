# Clinical Data Preparation for Ovarian Cancer Research

## Project Overview

This project focuses on preparing clinical data for a study involving women with active ovarian cancer undergoing chemotherapy. The clinical objective is to eventually predict emergency department (ED) visits or unanticipated hospital admissions (UHA) between chemotherapy appointments. My first project from my Statistical Programming I (R) BIOSTAT 721 course. 

Before predictive modeling can begin, clinical data must be cleaned, organized, and transformed into a reliable analytic dataset.

## Dataset Description

The project uses two datasets:

- **Patient-level dataset:** 50 patients with demographic information and medical histories.
- **Encounter-level dataset:** 550 clinical encounters containing information about office visits, emergency department visits, and hospitalizations.

The datasets were merged using a common patient identifier (MRN), producing an encounter-level analytic dataset.

## Methods and Data Processing

### 1. Data Integration and Exploration
- Imported and merged patient-level and encounter-level datasets using R.
- Examined dataset dimensions, variable types, and overall structure.
- Verified that the merged dataset preserved encounter-level observations.

### 2. Data Quality Assessment
- Assessed missing values across all variables.
- Identified 53 missing distress scores and 86 missing BMI measurements.
- Flagged 17 encounters associated with implausible patient ages.
- Flagged 6 encounters containing implausible BMI measurements.

Implausible BMI and date-of-birth values were flagged for review rather than automatically removed or modified.

### 3. White Blood Cell Count Processing
- Replaced 14 WBC measurements below the detection limit with a value of 1.
- Preserved original WBC measurements for documentation.
- Categorized WBC measurements into Low, Normal, High, and Not Taken groups.

### 4. Descriptive Analysis
- Generated an encounter-level frequency table summarizing WBC categories.
- Created a patient-level Table 1 summarizing race, ethnicity, financial class, hypertension, congestive heart failure, and diabetes.
- Formatted descriptive tables for presentation in a reproducible report.

## Selected Results

| WBC Category | Encounters | Percentage |
|---|---:|---:|
| Low | 54 | 9.8% |
| Normal | 436 | 79.3% |
| High | 60 | 10.9% |
| Not Taken | 0 | 0.0% |

Most encounters (79.3%) had WBC measurements within the defined normal range.

## Tools and Skills

- **R:** Data manipulation, cleaning, and descriptive statistics
- **R Markdown:** Reproducible statistical reporting
- **Data Integration:** Merging patient- and encounter-level datasets
- **Data Validation:** Missingness assessment and identification of implausible values
- **Data Visualization and Reporting:** Formatted summary tables using `gt` and `gtsummary`

## Project Scope

This project focused on creating and evaluating an analytic dataset for future predictive modeling. No predictive models were developed as part of this analysis.
