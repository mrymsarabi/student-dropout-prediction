
# Modeling Decisions

## 1. Research question

How effectively can classical machine-learning models predict students' final academic outcomes using information available at enrollment?

The target variable is `Target`, with three classes:

- `Graduate`
- `Dropout`
- `Enrolled`

This is a three-class classification problem.

## 2. Prediction point

The intended prediction point is enrollment.

The model should use only information that would reasonably be available at that time. Features recorded after enrollment must not be included in the enrollment-time model.

## 3. Excluded post-enrollment features

The following 12 features describe first- or second-semester activity or performance and will be excluded from the enrollment-time model:

- `Curricular units 1st sem (credited)`
- `Curricular units 1st sem (enrolled)`
- `Curricular units 1st sem (evaluations)`
- `Curricular units 1st sem (approved)`
- `Curricular units 1st sem (grade)`
- `Curricular units 1st sem (without evaluations)`
- `Curricular units 2nd sem (credited)`
- `Curricular units 2nd sem (enrolled)`
- `Curricular units 2nd sem (evaluations)`
- `Curricular units 2nd sem (approved)`
- `Curricular units 2nd sem (grade)`
- `Curricular units 2nd sem (without evaluations)`

The original dataset will remain unchanged.

## 4. Feature representation

Features are provisionally grouped as follows:

- Numerical measurements: grades, age, unemployment rate, inflation rate, and GDP.
- Categorical or binary features: demographic, educational, application, and other coded categories.
- Ordered feature: `Application order`, which represents the order of course preference.

These groups guide exploration and preprocessing. The final representations will be determined when the preprocessing pipeline is implemented.

## 5. Features requiring further timing verification

The UCI dataset description distinguishes information known at enrollment from academic performance recorded at the end of the first and second semesters. However, the available variable descriptions do not specify the exact recording time of every feature.

For the initial strict enrollment-time experiment, the following features will be excluded until their availability at the prediction point can be verified:

- `Debtor`
- `Tuition fees up to date`
- `Scholarship holder`

This is a conservative methodological decision. It does not mean that these features are necessarily post-enrollment variables.

If reliable documentation confirms that a feature was available at enrollment, it may be included in a separately documented experiment. The initial feature set will remain unchanged for the first baseline comparison.

## 6. Planned evaluation

The project will compare a simple baseline with classical machine-learning models.

Planned models:

- Dummy classifier baseline
- Logistic regression
- Decision tree
- Random forest

Planned evaluation measures:

- Macro-F1
- Recall for each target class
- Confusion matrix
- Accuracy as a secondary metric

Macro-F1 gives equal weight to each class's F1 score, which is useful when class frequencies differ.

## 7. Data splitting and preprocessing

The data will be split into training and test sets before fitting learned preprocessing operations.

Any encoders, scalers, or other transformations that learn from data will be fitted on the training data only. A scikit-learn pipeline will help keep preprocessing and model training together and reduce the risk of data leakage.

The test set will be held out for final evaluation rather than repeatedly used to make modeling decisions.

## 8. Interpretation and limitations

The dataset is observational. Associations between features and outcomes do not establish causation.

Model performance on this dataset does not automatically establish performance on other institutions, future cohorts, or a real student-support setting.

The project will report evaluation results and limitations rather than claiming that predictions are certain or that a feature causes dropout.

## 9. Status

Current status: exploratory data analysis and feature review.

The feature set is provisional until feature availability at enrollment has been verified.
