# Portfolio Execution Plan

This document defines the minimum work needed to turn the repository into a credible career asset for Data, AI/ML, and Physical AI roles.

## Priority Order

| Priority | Project | Why first |
|----------|---------|-----------|
| 1 | `projects/01_data_engineering_job_market_pipeline` | Broadest employability and strongest foundation for analytics and ML stories |
| 2 | `projects/04_physical_ai_ros2_vision_guided_manipulation` | Highest differentiation for robotics and Physical AI roles |
| 3 | `projects/02_tabular_ml_job_market_intelligence` | Converts data work into measurable ML outcomes |
| 4 | `projects/03_computer_vision_defect_detection` | Adds practical CV and edge inference evidence |

## What "Good Enough" Looks Like

### 1. Data Engineering Project

Minimum proof:

- ingest raw job listing data from one or more sources
- clean and normalize the data
- store curated tables in PostgreSQL, DuckDB, or a warehouse
- schedule or automate the pipeline
- produce one dashboard or analytical summary

Strong evidence:

- data quality checks
- containerized local setup
- architecture diagram
- documented schema

### 2. Physical AI Project

Minimum proof:

- ROS2 workspace with clear package structure
- one perception node
- one transform or pose-estimation step
- one action or planning step triggered by perception
- simulation demo with screenshots or short video

Strong evidence:

- TF tree explanation
- latency or FPS measurement
- failure cases
- Dockerized dev environment or reproducible setup notes

### 3. Tabular ML Project

Minimum proof:

- train/validation/test split
- baseline model and improved model
- metric comparison
- feature engineering notes
- confusion matrix or regression-error analysis

Strong evidence:

- experiment tracking
- inference script or small API
- business interpretation of results

### 4. Computer Vision Project

Minimum proof:

- dataset description
- training or fine-tuning workflow
- measurable evaluation
- qualitative failure-case review

Strong evidence:

- edge or optimized inference
- comparison between two model approaches
- deployment notes

## Repo-Level Rule

Do not claim a tool as part of the portfolio story unless at least one project shows:

- code
- metrics
- setup
- output

## Suggested 8-12 Week Sequence

| Weeks | Focus | Output |
|------|-------|--------|
| 1-3 | Data engineering project MVP | ETL + schema + first dashboard |
| 4-7 | ROS2 Physical AI MVP | Perception-to-action simulation demo |
| 8-10 | Tabular ML project | Baseline and tuned model with report |
| 11-12 | Computer vision project | Detection or defect-analysis pipeline |

## Hiring Outcome To Aim For

By the end of this plan, the repository should support a clear interview story:

`I built data pipelines, trained and evaluated ML systems, deployed perception workflows, and connected AI models to robotics-style decision and action loops.`
