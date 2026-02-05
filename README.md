# Wind Turbine Power Prediction (ENGIE Challenge)

## Overview

This project focuses on **predicting the active power produced by wind turbines** using operational sensor data and machine learning techniques. It is based on the **ENGIE / Collège de France Wind Energy Regression Challenge (2018)**, presented by Stéphane Mallat.

The main objective is to model the relationship between internal turbine measurements and power production, **without using wind speed data**, which is often unreliable for performance monitoring.

---

## Challenge Context

Wind power plays a critical role in addressing current and future climate challenges. As one of the largest wind power producers in France and Belgium, **ENGIE** aims to further optimize wind turbine performance by detecting abnormal deviations between expected and actual energy production.

This challenge explores data-driven approaches to predict turbine power output using only internal operational and environmental sensors.

---

## Problem Statement

Given 10-minute interval operational data from **four wind turbines (WT1–WT4)**, the task is to:

> **Predict the active power output of each turbine using regression models**, evaluated using **Mean Absolute Error (MAE)**.

Wind speed measurements are deliberately excluded from the feature set.

---

## Dataset Description

### Input Data (`engie_X.csv`)

Each row corresponds to a turbine at a given 10-minute timestamp and includes:

* **ID**: Unique identifier
* **MAC_CODE**: Turbine identifier (`WT1`, `WT2`, `WT3`, `WT4`)
* **Date_time**: 10-minute timestamp

#### Feature Categories

* **Temperatures (°C)**: gearbox bearings, generator components, nacelle, hub, rotor, etc.
* **Electrical measurements**: grid frequency, grid voltage
* **Rotational speeds**: rotor speed, generator speed, converter speed
* **Orientation variables**: wind direction, nacelle angle, pitch angle
* **Meteorological data**: outdoor temperature

Most variables include statistical summaries over 10 minutes:

* Average value
* Maximum (`_max`)
* Minimum (`_min`)
* Standard deviation (`_std`)

---

### Target Data (`engie_Y.csv`)

* **TARGET**: Active power output corresponding to each `ID`

Example:

```
ID;TARGET
1;0.1341
2;0.0461
```

---

## Evaluation Metric

The model performance is evaluated using **Mean Absolute Error (MAE)**:

[ MAE = \frac{1}{N} \sum_{i=1}^{N} |y_i - \hat{y}_i| ]

Lower MAE indicates better predictive performance.

---

## Methodology

Typical steps explored in this project include:

1. Data cleaning and preprocessing
2. Feature engineering and normalization
3. Model training (e.g. linear models, tree-based models, neural networks)
4. Cross-validation and hyperparameter tuning
5. Performance evaluation using MAE

---

## Repository Structure

```
├── data/              # Dataset files (not included if restricted)
├── notebooks/         # Exploratory analysis and experiments
├── src/               # Training and evaluation scripts
├── models/            # Saved models
├── results/           # Metrics and plots
└── README.md
```

---

## References

* ENGIE Wind Energy Regression Challenge (2018)
* Collège de France presentation by Stéphane Mallat
* Video: [https://www.youtube.com/watch?v=QTgE43q72f8](https://www.youtube.com/watch?v=QTgE43q72f8)

---

## License

This project is for **educational and research purposes only**. The dataset and challenge belong to ENGIE and their respective organizers.

---

## Acknowledgments

Thanks to **ENGIE** and the **Collège de France** for making this challenge publicly available and fostering research in renewable energy and machine learning.
