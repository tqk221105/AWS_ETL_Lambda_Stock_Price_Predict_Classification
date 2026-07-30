---
title: "Self-Assessment"
date: 2026-07-30
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

# Self-Assessment

From **08/06/2026 to 31/07/2026**, the team applied programming, databases, cloud computing, and machine learning to an end-to-end system. The project covered stock-data ingestion, validation and cleansing, feature engineering, XGBoost training, API serving, and dashboard visualization. This process strengthened the team's understanding of modular architecture, error handling, performance optimization, and integration across AWS services.

## Technical skill development

| Skill | Before the project | After the project | Evidence |
|:---|:---:|:---:|:---|
| AWS Lambda | Basic | Proficient | Designed multiple Lambda functions for separate pipeline stages |
| Amazon S3 | Basic | Proficient | Organized raw, cleansed, processed, quarantine, and model zones |
| Amazon SQS | Limited experience | Proficient | Implemented Fan-Out processing, ticker chunks, retries, and a DLQ-oriented design |
| Amazon EventBridge | Limited experience | Proficient | Scheduled the daily market-data update workflow |
| Amazon API Gateway | Basic | Proficient | Exposed prediction results through a REST API |
| Amazon ECR / Docker | Basic | Proficient | Packaged data and ML dependencies as Lambda container images |
| Data Quality | Basic | Proficient | Added schema validation, business rules, and quarantine handling |
| Feature Engineering | Basic | Proficient | Created 16 technical indicators while controlling look-ahead bias |
| XGBoost / Machine Learning | Basic | Proficient | Trained and evaluated a binary classifier and stored model artifacts |
| Apache Parquet / Polars | Limited experience | Proficient | Improved storage efficiency and large time-series processing performance |
| Hugo documentation | Limited experience | Proficient | Structured a bilingual, step-by-step workshop report |

## Assessment by criteria

| # | Criterion | Assessment | Good | Fair | Average |
|:--:|:---|:---|:--:|:--:|:--:|
| 1 | Professional knowledge and skills | Applied AWS architecture, data engineering, and ML knowledge to an integrated system |  | ✓ |  |
| 2 | Ability to learn | Quickly learned AWS services, Polars, Parquet, XGBoost, and Hugo | ✓ |  |  |
| 3 | Proactiveness | Researched solutions for Lambda timeout, invalid data, and dependency packaging | ✓ |  |  |
| 4 | Responsibility | Followed progress and completed assigned modules and documentation | ✓ |  |  |
| 5 | Discipline | Followed source-code conventions, data structures, and team assignments |  | ✓ |  |
| 6 | Progressive mindset | Accepted review comments and iteratively improved architecture and documentation | ✓ |  |  |
| 7 | Communication | Communicated work clearly, but technical issue reports should be more concise |  | ✓ |  |
| 8 | Teamwork | Coordinated ingestion, ETL, ML, API, dashboard, and documentation work | ✓ |  |  |
| 9 | Professional conduct | Respected contributions and maintained a collaborative attitude | ✓ |  |  |
| 10 | Problem solving | Identified causes and proposed solutions; automated testing and measurement need improvement |  | ✓ |  |
| 11 | Contribution to the project | Delivered an end-to-end pipeline, workshop documentation, and replay/testing tools | ✓ |  |  |
| 12 | Overall assessment | Met the learning objectives and produced a system that can be extended |  | ✓ |  |

## What the team did well

- Decomposed a large problem into ingestion, quality-gate, ETL, ML, serving, and dashboard pipelines.
- Used Lambda and SQS Fan-Out to process thousands of tickers without relying on one long-running function.
- Protected downstream data with validation rules and a quarantine path.
- Used Parquet and Polars to improve storage and time-series processing efficiency.
- Maintained a README, bilingual Hugo workshop, and worklog so the system can be followed and reproduced.
- Coordinated independent modules and integrated them into one end-to-end workflow.

## Areas for improvement

- The current **53.12% Accuracy** and **0.5487 AUC-ROC** indicate a weak signal. The next iteration needs a clear baseline, feature selection, walk-forward validation, and comparison with additional models.
- Add backtesting with transaction costs, slippage, liquidity limits, and a Buy-and-Hold benchmark.
- Increase automated unit, integration, and end-to-end data tests.
- Standardize infrastructure deployment with AWS SAM, CDK, or Terraform.
- Complete CloudWatch dashboards, alarms, DLQ metrics, and alerts for missing or failed data runs.
- Make technical reports more precise about assumptions, measurements, limitations, and the difference between experimental results and investment recommendations.

## Key lessons learned

- Architecture must begin with service limits, data volume, and failure-recovery requirements.
- Validation, logging, and replay capability are as important as the main transformation logic.
- Time-series splitting and future-leakage controls determine whether model results are trustworthy.
- Accuracy slightly above 50% does not imply a profitable strategy or justify an investment decision.
- Clear documentation, shared conventions, and regular communication reduce integration errors and save time.

## Overall conclusion

The project achieved its learning objective and delivered a functional foundation, but it is not yet a production trading system. The most important next step is to improve reliability and evaluation discipline before expanding features: stronger automated tests, observable infrastructure, reproducible deployment, and realistic backtesting should take priority over adding model complexity.
