1️⃣ Project Constraints & Objectives (cleaned)
Context

Project on wind power production prediction

Dataset contains 4 wind turbines

Strong recommendation: work with only one turbine

Minimum required data:

10k–20k samples

We will use 20,000 samples from WT1

Educational constraints

No literature review in the report

Focus on:

Data understanding

Methodology

Experimental protocol

Results and interpretation

Quality of writing is very important

Deadline: 6 weeks from 24/12/2025

Project counts for 2/3 of final grade

2️⃣ Technical & Methodological Pipeline
Dataset preparation

Start from engie_X.csv and engie_Y.csv

Concatenate X and Y using ID

Filter:

Only WT1

Only 20,000 samples

Initial testing:

First test models on 1,000 samples (sanity check)

Then scale to full 20,000

Data preprocessing

Identify missing values

List variables with missing values

Decide whether to:

Keep and impute

Or remove variables

Imputation strategy:

Simple imputation (mean or median)

Be careful not to bias learning

Remove:

Null or negative power production values

Separate again into:

Features X

Target y

Models to implement

You do not explain model internals, only usage.

Required models:

Linear Regression / classical ML regression

Deep Neural Network (DNN)

Additional required capability

The model must be able to:

Indicate when it is not operating optimally, based on current behavior

Examples:

High prediction error

Out-of-distribution inputs

Abnormal sensor patterns

(Implementation can be simple: error thresholding, residual analysis, confidence proxy)

Experimental protocol

Must be clearly defined and justified:

Train / validation / test split

Evaluation metric:

MAE (mandatory, per challenge statement)

Comparison between models

Performance analysis

3️⃣ Deliverables (very important)
✅ Code deliverables

Well-documented Python code

A Google Colab–ready notebook

Notebook must:

Load the 20,000-row dataset

Run end-to-end:

Preprocessing

Training

Evaluation

Visualization of results

✅ Report deliverable (LaTeX)
Format

LaTeX (.tex) file

Length: 10–20 pages

Clean academic style

No literature review

Mandatory structure

Problem description

Dataset description

Data preprocessing

Experimental protocol

Models

Results

Conclusion (lessons learned)

Author & project info (must be included)

Project title: Wind Power Prediction using Deep Learning

Course: Deep Learning

School: École Centrale Casablanca

Authors:

OUANZOUGUI Abdelhak

EL ABDI Ibrahim