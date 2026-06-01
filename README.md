# Mushroom Classification Group Project

This folder contains a complete, self-contained solution for the mushroom classification group project.

## Contents

- `data/raw/mushroom_classification_data.csv`: original dataset file
- `data/processed/mushroom_classification_clean.csv`: cleaned dataset used for modelling
- `notebooks/mushroom_classification_project.ipynb`: final notebook with report and code
- `report.md`: short standalone final report
- `requirements.txt`: Python package requirements

## Project Summary

The task is a supervised binary classification problem. The target variable is `poison`, where `e` means edible and `p` means poisonous. All input variables are categorical mushroom characteristics.

The notebook documents loading, data-quality checks, cleaning, preprocessing, model training, evaluation, interpretation, and transparent documentation of LLM support.

## Notes for Submission

Open and run the notebook from the `notebooks` directory so the relative paths to `../data/...` work as expected.
