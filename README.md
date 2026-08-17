
# Instructor Effectiveness Modeling 

## Project Overview

This project analyzes instructor effectiveness in an EdTech environment where multiple instructors teach different course batches.

The objective is to use learner outcomes, engagement metrics, and feedback data to:

- Explore patterns in learner and batch performance
- Define an Instructor Effectiveness Score
- Aggregate batch-level data to instructor level
- Classify instructors into Low, Medium, and High effectiveness tiers
- Build a machine learning model to predict effectiveness tiers
- Interpret the factors influencing the predictions
- Discuss limitations and responsible use of the model

> **Note:** This project was originally developed as part of a Data Science / AI Content Specialist assessment.

---

## Problem Statement

An EdTech platform runs the same or different courses across multiple batches taught by different instructors.

Each instructor may teach:

- Multiple batches
- The same course across different batches
- Different courses over time

The goal is to estimate instructor effectiveness using available learner outcomes, engagement, and feedback data.

Since there is no predefined effectiveness label, the project requires designing a reasonable effectiveness score and converting it into effectiveness tiers.

---

## Dataset

Each row in the dataset represents one course batch.

### Identifier Variables

- `batch_id` — Unique batch identifier
- `instructor_id` — Unique instructor identifier
- `course_id` — Course identifier

### Learner Outcome Metrics

- `completion_rate`
- `dropout_rate`
- `avg_score_improvement`
- `avg_quiz_score`

### Engagement Metrics

- `avg_watch_time`
- `assignment_submission_rate`
- `forum_activity_rate`

### Feedback Metrics

- `avg_feedback_score`
- `feedback_response_rate`

> The original assessment dataset is not included in this repository.

---

## Methodology

The project follows the following workflow:

```text
Batch-Level Data
       ↓
Data Cleaning & EDA
       ↓
Effectiveness Score
       ↓
Batch → Instructor Aggregation
       ↓
Low / Medium / High Tiers
       ↓
Feature Engineering
       ↓
Train/Test Split
       ↓
Logistic Regression
       ↓
Model Evaluation
       ↓
Feature Importance
       ↓
Business Interpretation & Limitations
