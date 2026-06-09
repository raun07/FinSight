# FinSight — Retail Banking Risk & Customer Intelligence Platform

An end-to-end BFSI analytics platform built on 1.33M Lending Club loan records.
Covers credit risk scoring, portfolio analytics, and automated executive reporting.

## Business Problem
A retail bank needs to identify which loan applicants are likely to default (21.41%
current default rate), understand concentration risk across loan grades and purposes,
and automate weekly risk reporting for senior management.

## Results
| Model | Metric | Score |
|-------|--------|-------|
| Credit Risk (XGBoost) | AUC-ROC | 0.72 |
| Risk tier classification | 4 tiers | Low / Medium / High / Critical |

## Key Findings
- Grade C loans = largest portfolio segment with 24% default = highest absolute exposure ($1.35B)
- Small business loans default at 31.5% vs 18.2% for credit cards
- High DTI (>30%) borrowers default at 31.24% vs 16.22% for low DTI
- 2016-2017 vintage cohorts show 25-27% default — underwriting loosened during peak growth
- Unknown employment history = 28.86% default — missing data is itself a risk signal

## Tech Stack
Python (Pandas, sklearn, XGBoost, DuckDB) · SQL · MS Excel (Power Query) ·
Power BI (DAX) · Automated PDF Report Generation

## Project Structure
- notebooks/ — Data cleaning, SQL analytics, ML model, AI report
- data/outputs/ — SQL query results (8 business queries)
- models/ — Trained XGBoost credit risk model
- reports/ — Excel report, Power BI dashboard PDF, weekly risk report PDF

## Dataset
Lending Club Loan Data (890K+ records, 2007-2018)
Source: kaggle.com/datasets/adarshsng/lending-club-loan-data-csv
