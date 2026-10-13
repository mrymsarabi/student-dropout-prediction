# Data Dictionary and Feature Inventory

## Dataset Information

- **Dataset:** Predict Students' Dropout and Academic Success
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)
- **Observations:** 4,424 students
- **Columns:** 37, including 36 original features and the target
- **Target variable:** `Target`
- **Target classes:** Dropout, Enrolled, Graduate

## Target Definition

`Target` represents the final outcome category: Dropout, Enrolled, or Graduate.

## Feature Inventory

The full feature definitions and category codes should be checked against the original UCI dataset documentation.

| Feature | Meaning | Data type | Available at enrollment? | Modeling decision |
|---|---|---|---|---|
| Age at enrollment | Student's age at enrollment | Numerical | Yes | Candidate to include |
| Previous qualification | Student's previous qualification | Categorical code | Yes | Candidate to include |
| Previous qualification (grade) | Grade associated with previous qualification | Numerical | Yes | Candidate to include |
| Admission grade | Grade associated with admission | Numerical | Yes | Candidate to include |
| Course | Enrolled course/program | Categorical code | Yes | Candidate to include |
| Application mode | Admission/application route | Categorical code | Yes | Candidate to include |
| Curricular units 1st sem (grade) | First-semester academic performance | Numerical | No | Exclude |
| Curricular units 2nd sem (grade) | Second-semester academic performance | Numerical | No | Exclude |

*This is an initial inventory, not the complete feature list. Verify each feature's definition and timing before finalizing the modeling decisions.*

## Notes

- Numeric codes do not necessarily represent numerical quantities.
- Semester-related features will be excluded from the enrollment-time prediction model to prevent temporal data leakage.
- The original dataset will remain unchanged.
- Modeling decisions will be documented as the project develops.