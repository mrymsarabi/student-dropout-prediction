# Modeling Decisions

## Prediction Objective

Predict students' final academic outcomes using information available at enrollment.

## Target

`Target`, with three classes: Dropout, Enrolled, and Graduate.

## Feature Timing

First- and second-semester academic performance features will be excluded from the enrollment-time model because they are recorded after enrollment.

## Evaluation

Macro-F1 and per-class recall will be used alongside accuracy because the target classes have different frequencies.

## Pending Decisions

- Verify the timing of financial-status and economic-context features.
- Finalize categorical and numerical feature types.
- Choose preprocessing methods.
- Establish the train-test split and model-selection procedure.