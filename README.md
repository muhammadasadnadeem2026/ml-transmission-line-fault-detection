# Transmission-Line Fault Detection with Machine Learning

> Five classifiers learn to recognise the fault type on a transmission line from three-phase currents and voltages.
> **Best: decision tree, 89.5% test accuracy.**

## Results (test set, 80:20 split)

| Model | Test accuracy | F1-score |
|---|---|---|
| **Decision tree** | **89.45%** | **89.43%** |
| Random forest | 88.62% | 88.63% |
| Naive Bayes | 80.48% | 76.27% |
| Support vector machine | 75.97% | 73.41% |
| Logistic regression | 35.92% | 24.11% |

- Six classes: no fault, LG, LL, LLG, LLL, LLLG
- Simulated system: four 11 kV generators, transformers, fault at the line midpoint
- Logistic regression fails, showing the fault boundaries are strongly non-linear

## Repository structure

```
src/electrical_fault_analysis.py   EDA, preprocessing, training, evaluation and feature importance
data/                              Put classData.csv here (see data/README.md)
```

## Run

```bash
pip install -r requirements.txt
python src/electrical_fault_analysis.py
```

## Licence

Copyright © 2025 Muhammad Asad Nadeem. All rights reserved.
The code is shared for viewing as part of my engineering portfolio. Please contact me before reusing it.
