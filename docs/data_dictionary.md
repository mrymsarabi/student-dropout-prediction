# Data Dictionary

## 1. Dataset overview

This document describes the variables in the **Predict Students' Dropout
and Academic Success** dataset using the variable table and category
definitions published on the UCI Machine Learning Repository page.

-   **Source:** [UCI Machine Learning Repository --- Predict Students'
    Dropout and Academic
    Success](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success)
-   **Prediction target:** `Target`
-   **Task described by the source:** Three-category classification of
    the student's final outcome: `Dropout`, `Enrolled`, or `Graduate`.
-   **Missing values:** The source variable table marks every listed
    variable as having no missing values.

The dataset contains student demographic, educational, admission,
family-background, financial-status, and economic-context variables. It
also contains variables describing academic performance during the first
and second semesters.

## 2. Important notes for this project

The research question for this project is:

> How effectively can classical machine-learning models predict
> students' final academic outcomes using information available at
> enrollment?

For that reason, the planned enrollment-time model will **exclude all 12
first- and second-semester variables**. They describe information
recorded after enrollment and would not be available at the intended
prediction point. This is a modeling decision for this project, not a
change to the original dataset.

The original dataset should remain unchanged. Any feature selection or
preprocessing should be performed on a separate modeling DataFrame.

Some variable names and descriptions below preserve the wording used in
the UCI variable table. For example, the source spells `Nacionality`
that way. The second-semester "without evaluations" description also
says "in the 1st semester" in the source table; this apparent
inconsistency is recorded in the notes rather than silently corrected.

## 3. Variable inventory

The tables below reproduce the source's variable roles, types,
demographic groupings, descriptions, units where supplied, and
missing-value flags. Category codes are documented in Section 4.

  ---------------------------------------------------------------------------------------
  Variable name     Role        Type          Demographic   Description /     Missing
                                              grouping      units             values
                                                                              (source)
  ----------------- ----------- ------------- ------------- ----------------- -----------
  Marital Status    Feature     Integer       Marital       Coded marital     No
                                              Status        status; see       
                                                            Section 4.1.      

  Application mode  Feature     Integer       ---           Coded application No
                                                            mode; see Section 
                                                            4.2.              

  Application order Feature     Integer       ---           Application order No
                                                            (between 0 ---    
                                                            first choice; and 
                                                            9 --- last        
                                                            choice).          

  Course            Feature     Integer       ---           Coded             No
                                                            course/program;   
                                                            see Section 4.4.  

  Daytime/evening   Feature     Integer       ---           1 --- daytime; 0  No
  attendance                                                --- evening.      

  Previous          Feature     Integer       Education     Coded previous    No
  qualification                               Level         qualification;    
                                                            see Section 4.6.  

  Previous          Feature     Continuous    ---           Grade of previous No
  qualification                                             qualification     
  (grade)                                                   (between 0 and    
                                                            200).             

  Nacionality       Feature     Integer       Nationality   Coded             No
                                                            nationality; see  
                                                            Section 4.8.      

  Mother's          Feature     Integer       Education     Coded mother's    No
  qualification                               Level         qualification;    
                                                            see Section 4.9.  

  Father's          Feature     Integer       Education     Coded father's    No
  qualification                               Level         qualification;    
                                                            see Section 4.10. 

  Mother's          Feature     Integer       Occupation    Coded mother's    No
  occupation                                                occupation; see   
                                                            Section 4.11.     

  Father's          Feature     Integer       Occupation    Coded father's    No
  occupation                                                occupation; see   
                                                            Section 4.12.     

  Admission grade   Feature     Continuous    ---           Admission grade   No
                                                            (between 0 and    
                                                            200).             

  Displaced         Feature     Integer       ---           1 --- yes; 0 ---  No
                                                            no.               

  Educational       Feature     Integer       ---           1 --- yes; 0 ---  No
  special needs                                             no.               

  Debtor            Feature     Integer       ---           1 --- yes; 0 ---  No
                                                            no.               

  Tuition fees up   Feature     Integer       ---           1 --- yes; 0 ---  No
  to date                                                   no.               

  Gender            Feature     Integer       Gender        1 --- male; 0 --- No
                                                            female.           

  Scholarship       Feature     Integer       ---           1 --- yes; 0 ---  No
  holder                                                    no.               

  Age at enrollment Feature     Integer       Age           Age of student at No
                                                            enrollment.       

  International     Feature     Integer       ---           1 --- yes; 0 ---  No
                                                            no.               

  Curricular units  Feature     Integer       ---           Number of         No
  1st sem                                                   curricular units  
  (credited)                                                credited in the   
                                                            1st semester.     

  Curricular units  Feature     Integer       ---           Number of         No
  1st sem                                                   curricular units  
  (enrolled)                                                enrolled in the   
                                                            1st semester.     

  Curricular units  Feature     Integer       ---           Number of         No
  1st sem                                                   evaluations to    
  (evaluations)                                             curricular units  
                                                            in the 1st        
                                                            semester.         

  Curricular units  Feature     Integer       ---           Number of         No
  1st sem                                                   curricular units  
  (approved)                                                approved in the   
                                                            1st semester.     

  Curricular units  Feature     Integer       ---           Grade average in  No
  1st sem (grade)                                           the 1st semester  
                                                            (between 0 and    
                                                            20).              

  Curricular units  Feature     Integer       ---           Number of         No
  1st sem (without                                          curricular units  
  evaluations)                                              without           
                                                            evaluations in    
                                                            the 1st semester. 

  Curricular units  Feature     Integer       ---           Number of         No
  2nd sem                                                   curricular units  
  (credited)                                                credited in the   
                                                            2nd semester.     

  Curricular units  Feature     Integer       ---           Number of         No
  2nd sem                                                   curricular units  
  (enrolled)                                                enrolled in the   
                                                            2nd semester.     

  Curricular units  Feature     Integer       ---           Number of         No
  2nd sem                                                   evaluations to    
  (evaluations)                                             curricular units  
                                                            in the 2nd        
                                                            semester.         

  Curricular units  Feature     Integer       ---           Number of         No
  2nd sem                                                   curricular units  
  (approved)                                                approved in the   
                                                            2nd semester.     

  Curricular units  Feature     Integer       ---           Grade average in  No
  2nd sem (grade)                                           the 2nd semester  
                                                            (between 0 and    
                                                            20).              

  Curricular units  Feature     Integer       ---           Number of         No
  2nd sem (without                                          curricular units  
  evaluations)                                              without           
                                                            evaluations in    
                                                            the 1st semester  
                                                            (wording as given 
                                                            in the source).   

  Unemployment rate Feature     Continuous    ---           Unemployment rate No
                                                            (%).              

  Inflation rate    Feature     Continuous    ---           Inflation rate    No
                                                            (%).              

  GDP               Feature     Continuous    ---           GDP.              No

  Target            Target      Categorical   ---           Final outcome;    No
                                                            three-category    
                                                            classification    
                                                            task: dropout,    
                                                            enrolled, and     
                                                            graduate at the   
                                                            end of the normal 
                                                            duration of the   
                                                            course.           
  ---------------------------------------------------------------------------------------

## 4. Categorical code definitions

The code meanings in this section follow the UCI variable table supplied
for this dictionary. Codes are categorical labels; they should not
automatically be treated as measurements where a larger number means a
larger amount.

### 4.1 Marital Status

    Code Meaning
  ------ -------------------
       1 Single
       2 Married
       3 Widower
       4 Divorced
       5 Facto union
       6 Legally separated

### 4.2 Application mode

    Code Meaning
  ------ -----------------------------------------------------
       1 1st phase --- general contingent
       2 Ordinance No. 612/93
       5 1st phase --- special contingent (Azores Island)
       7 Holders of other higher courses
      10 Ordinance No. 854-B/99
      15 International student (bachelor)
      16 1st phase --- special contingent (Madeira Island)
      17 2nd phase --- general contingent
      18 3rd phase --- general contingent
      26 Ordinance No. 533-A/99, item b2) (Different Plan)
      27 Ordinance No. 533-A/99, item b3 (Other Institution)
      39 Over 23 years old
      42 Transfer
      43 Change of course
      44 Technological specialization diploma holders
      51 Change of institution/course
      53 Short cycle diploma holders
      57 Change of institution/course (International)

### 4.3 Application order

The source describes this as application order from **0 --- first
choice** to **9 --- last choice**. The source does not provide a
separate meaning for every intermediate code in the supplied table.

### 4.4 Course

    Code Meaning
  ------ --------------------------------------
      33 Biofuel Production Technologies
     171 Animation and Multimedia Design
    8014 Social Service (evening attendance)
    9003 Agronomy
    9070 Communication Design
    9085 Veterinary Nursing
    9119 Informatics Engineering
    9130 Equinculture
    9147 Management
    9238 Social Service
    9254 Tourism
    9500 Nursing
    9556 Oral Hygiene
    9670 Advertising and Marketing Management
    9773 Journalism and Communication
    9853 Basic Education
    9991 Management (evening attendance)

### 4.5 Daytime/evening attendance

    Code Meaning
  ------ ---------
       1 Daytime
       0 Evening

### 4.6 Previous qualification

    Code Meaning
  ------ --------------------------------------------------------------
       1 Secondary education
       2 Higher education --- bachelor's degree
       3 Higher education --- degree
       4 Higher education --- master's
       5 Higher education --- doctorate
       6 Frequency of higher education
       9 12th year of schooling --- not completed
      10 11th year of schooling --- not completed
      12 Other --- 11th year of schooling
      14 10th year of schooling
      15 10th year of schooling --- not completed
      19 Basic education 3rd cycle (9th/10th/11th year) or equivalent
      38 Basic education 2nd cycle (6th/7th/8th year) or equivalent
      39 Technological specialization course
      40 Higher education --- degree (1st cycle)
      42 Professional higher technical course
      43 Higher education --- master (2nd cycle)

### 4.7 Previous qualification (grade)

A continuous variable described as the grade of the previous
qualification, between 0 and 200.

### 4.8 Nacionality

    Code Meaning
  ------ -----------------------
       1 Portuguese
       2 German
       6 Spanish
      11 Italian
      13 Dutch
      14 English
      17 Lithuanian
      21 Angolan
      22 Cape Verdean
      24 Guinean
      25 Mozambican
      26 Santomean
      32 Turkish
      41 Brazilian
      62 Romanian
     100 Moldova (Republic of)
     101 Mexican
     103 Ukrainian
     105 Russian
     108 Cuban
     109 Colombian

### 4.9 Mother's qualification

    Code Meaning
  ------ --------------------------------------------------------------
       1 Secondary Education --- 12th Year of Schooling or Eq.
       2 Higher Education --- Bachelor's Degree
       3 Higher Education --- Degree
       4 Higher Education --- Master's
       5 Higher Education --- Doctorate
       6 Frequency of Higher Education
       9 12th Year of Schooling --- Not Completed
      10 11th Year of Schooling --- Not Completed
      11 7th Year (Old)
      12 Other --- 11th Year of Schooling
      14 10th Year of Schooling
      18 General commerce course
      19 Basic Education 3rd Cycle (9th/10th/11th Year) or Equivalent
      22 Technical-professional course
      26 7th year of schooling
      27 2nd cycle of the general high school course
      29 9th Year of Schooling --- Not Completed
      30 8th year of schooling
      34 Unknown
      35 Can't read or write
      36 Can read without having a 4th year of schooling
      37 Basic education 1st cycle (4th/5th year) or equivalent
      38 Basic Education 2nd Cycle (6th/7th/8th Year) or Equivalent
      39 Technological specialization course
      40 Higher education --- degree (1st cycle)
      41 Specialized higher studies course
      42 Professional higher technical course
      43 Higher Education --- Master (2nd cycle)
      44 Higher Education --- Doctorate (3rd cycle)

### 4.10 Father's qualification

    Code Meaning
  ------ --------------------------------------------------------------
       1 Secondary Education --- 12th Year of Schooling or Eq.
       2 Higher Education --- Bachelor's Degree
       3 Higher Education --- Degree
       4 Higher Education --- Master's
       5 Higher Education --- Doctorate
       6 Frequency of Higher Education
       9 12th Year of Schooling --- Not Completed
      10 11th Year of Schooling --- Not Completed
      11 7th Year (Old)
      12 Other --- 11th Year of Schooling
      13 2nd year complementary high school course
      14 10th Year of Schooling
      18 General commerce course
      19 Basic Education 3rd Cycle (9th/10th/11th Year) or Equivalent
      20 Complementary High School Course
      22 Technical-professional course
      25 Complementary High School Course --- not concluded
      26 7th year of schooling
      27 2nd cycle of the general high school course
      29 9th Year of Schooling --- Not Completed
      30 8th year of schooling
      31 General Course of Administration and Commerce
      33 Supplementary Accounting and Administration
      34 Unknown
      35 Can't read or write
      36 Can read without having a 4th year of schooling
      37 Basic education 1st cycle (4th/5th year) or equivalent
      38 Basic Education 2nd Cycle (6th/7th/8th Year) or Equivalent
      39 Technological specialization course
      40 Higher education --- degree (1st cycle)
      41 Specialized higher studies course
      42 Professional higher technical course
      43 Higher Education --- Master (2nd cycle)
      44 Higher Education --- Doctorate (3rd cycle)

### 4.11 Mother's occupation

  -----------------------------------------------------------------------
                                      Code Meaning
  ---------------------------------------- ------------------------------
                                         0 Student

                                         1 Representatives of the
                                           Legislative Power and
                                           Executive Bodies, Directors,
                                           Directors and Executive
                                           Managers

                                         2 Specialists in Intellectual
                                           and Scientific Activities

                                         3 Intermediate Level Technicians
                                           and Professions

                                         4 Administrative staff

                                         5 Personal Services, Security
                                           and Safety Workers and Sellers

                                         6 Farmers and Skilled Workers in
                                           Agriculture, Fisheries and
                                           Forestry

                                         7 Skilled Workers in Industry,
                                           Construction and Craftsmen

                                         8 Installation and Machine
                                           Operators and Assembly Workers

                                         9 Unskilled Workers

                                        10 Armed Forces Professions

                                        90 Other Situation

                                        99 (blank)

                                       122 Health professionals

                                       123 Teachers

                                       125 Specialists in information and
                                           communication technologies
                                           (ICT)

                                       131 Intermediate level science and
                                           engineering technicians and
                                           professions

                                       132 Technicians and professionals,
                                           of intermediate level of
                                           health

                                       134 Intermediate level technicians
                                           from legal, social, sports,
                                           cultural and similar services

                                       141 Office workers, secretaries in
                                           general and data processing
                                           operators

                                       143 Data, accounting, statistical,
                                           financial services and
                                           registry-related operators

                                       144 Other administrative support
                                           staff

                                       151 Personal service workers

                                       152 Sellers

                                       153 Personal care workers and the
                                           like

                                       171 Skilled construction workers
                                           and the like, except
                                           electricians

                                       173 Skilled workers in printing,
                                           precision instrument
                                           manufacturing, jewelers,
                                           artisans and the like

                                       175 Workers in food processing,
                                           woodworking, clothing and
                                           other industries and crafts

                                       191 Cleaning workers

                                       192 Unskilled workers in
                                           agriculture, animal
                                           production, fisheries and
                                           forestry

                                       193 Unskilled workers in
                                           extractive industry,
                                           construction, manufacturing
                                           and transport

                                       194 Meal preparation assistants
  -----------------------------------------------------------------------

### 4.12 Father's occupation

  -----------------------------------------------------------------------
                                      Code Meaning
  ---------------------------------------- ------------------------------
                                         0 Student

                                         1 Representatives of the
                                           Legislative Power and
                                           Executive Bodies, Directors,
                                           Directors and Executive
                                           Managers

                                         2 Specialists in Intellectual
                                           and Scientific Activities

                                         3 Intermediate Level Technicians
                                           and Professions

                                         4 Administrative staff

                                         5 Personal Services, Security
                                           and Safety Workers and Sellers

                                         6 Farmers and Skilled Workers in
                                           Agriculture, Fisheries and
                                           Forestry

                                         7 Skilled Workers in Industry,
                                           Construction and Craftsmen

                                         8 Installation and Machine
                                           Operators and Assembly Workers

                                         9 Unskilled Workers

                                        10 Armed Forces Professions

                                        90 Other Situation

                                        99 (blank)

                                       101 Armed Forces Officers

                                       102 Armed Forces Sergeants

                                       103 Other Armed Forces personnel

                                       112 Directors of administrative
                                           and commercial services

                                       114 Hotel, catering, trade and
                                           other services directors

                                       121 Specialists in the physical
                                           sciences, mathematics,
                                           engineering and related
                                           techniques

                                       122 Health professionals

                                       123 Teachers

                                       124 Specialists in finance,
                                           accounting, administrative
                                           organization, public and
                                           commercial relations

                                       131 Intermediate level science and
                                           engineering technicians and
                                           professions

                                       132 Technicians and professionals,
                                           of intermediate level of
                                           health

                                       134 Intermediate level technicians
                                           from legal, social, sports,
                                           cultural and similar services

                                       135 Information and communication
                                           technology technicians

                                       141 Office workers, secretaries in
                                           general and data processing
                                           operators

                                       143 Data, accounting, statistical,
                                           financial services and
                                           registry-related operators

                                       144 Other administrative support
                                           staff

                                       151 Personal service workers

                                       152 Sellers

                                       153 Personal care workers and the
                                           like

                                       154 Protection and security
                                           services personnel

                                       161 Market-oriented farmers and
                                           skilled agricultural and
                                           animal production workers

                                       163 Farmers, livestock keepers,
                                           fishermen, hunters and
                                           gatherers, subsistence

                                       171 Skilled construction workers
                                           and the like, except
                                           electricians

                                       172 Skilled workers in metallurgy,
                                           metalworking and similar

                                       174 Skilled workers in electricity
                                           and electronics

                                       175 Workers in food processing,
                                           woodworking, clothing and
                                           other industries and crafts

                                       181 Fixed plant and machine
                                           operators

                                       182 Assembly workers

                                       183 Vehicle drivers and mobile
                                           equipment operators

                                       192 Unskilled workers in
                                           agriculture, animal
                                           production, fisheries and
                                           forestry

                                       193 Unskilled workers in
                                           extractive industry,
                                           construction, manufacturing
                                           and transport

                                       194 Meal preparation assistants

                                       195 Street vendors (except food)
                                           and street service providers
  -----------------------------------------------------------------------

### 4.13 Admission grade

A continuous variable described as the admission grade, between 0 and
200.

### 4.14 Binary yes/no features

The source defines the following variables with the same coding:

  Variable                    Code 1   Code 0
  --------------------------- -------- --------
  Displaced                   Yes      No
  Educational special needs   Yes      No
  Debtor                      Yes      No
  Tuition fees up to date     Yes      No
  Scholarship holder          Yes      No
  International               Yes      No

### 4.15 Gender

    Code Meaning
  ------ ---------
       1 Male
       0 Female

### 4.16 Age at enrollment

Integer variable described as the student's age at enrollment. The
source table does not specify a unit separately.

### 4.17 First-semester curricular-unit variables

  -----------------------------------------------------------------------
  Variable                            Source description
  ----------------------------------- -----------------------------------
  Curricular units 1st sem (credited) Number of curricular units credited
                                      in the 1st semester

  Curricular units 1st sem (enrolled) Number of curricular units enrolled
                                      in the 1st semester

  Curricular units 1st sem            Number of evaluations to curricular
  (evaluations)                       units in the 1st semester

  Curricular units 1st sem (approved) Number of curricular units approved
                                      in the 1st semester

  Curricular units 1st sem (grade)    Grade average in the 1st semester
                                      (between 0 and 20)

  Curricular units 1st sem (without   Number of curricular units without
  evaluations)                        evaluations in the 1st semester
  -----------------------------------------------------------------------

### 4.18 Second-semester curricular-unit variables

  -----------------------------------------------------------------------
  Variable                            Source description
  ----------------------------------- -----------------------------------
  Curricular units 2nd sem (credited) Number of curricular units credited
                                      in the 2nd semester

  Curricular units 2nd sem (enrolled) Number of curricular units enrolled
                                      in the 2nd semester

  Curricular units 2nd sem            Number of evaluations to curricular
  (evaluations)                       units in the 2nd semester

  Curricular units 2nd sem (approved) Number of curricular units approved
                                      in the 2nd semester

  Curricular units 2nd sem (grade)    Grade average in the 2nd semester
                                      (between 0 and 20)

  Curricular units 2nd sem (without   Number of curricular units without
  evaluations)                        evaluations in the 1st semester
                                      (wording as given in the source)
  -----------------------------------------------------------------------

### 4.19 Economic indicators

  Variable            Type in source   Description / units in source
  ------------------- ---------------- -------------------------------
  Unemployment rate   Continuous       Unemployment rate (%)
  Inflation rate      Continuous       Inflation rate (%)
  GDP                 Continuous       GDP

### 4.20 Target

The target variable is named `Target`. The source describes it as a
categorical variable for a three-category classification task. The
possible outcomes are:

  Target class   Meaning
  -------------- -------------------------------------
  Dropout        Student's final outcome is dropout
  Enrolled       Student's final outcome is enrolled
  Graduate       Student's final outcome is graduate

The source describes the target as the outcome at the end of the normal
duration of the course.

## 5. Feature-selection note for the enrollment-time prediction task

For the project's stated prediction point---enrollment---the following
12 variables are excluded from the initial model because they describe
first- or second-semester activity or performance:

1.  `Curricular units 1st sem (credited)`
2.  `Curricular units 1st sem (enrolled)`
3.  `Curricular units 1st sem (evaluations)`
4.  `Curricular units 1st sem (approved)`
5.  `Curricular units 1st sem (grade)`
6.  `Curricular units 1st sem (without evaluations)`
7.  `Curricular units 2nd sem (credited)`
8.  `Curricular units 2nd sem (enrolled)`
9.  `Curricular units 2nd sem (evaluations)`
10. `Curricular units 2nd sem (approved)`
11. `Curricular units 2nd sem (grade)`
12. `Curricular units 2nd sem (without evaluations)`

This exclusion is intended to prevent **temporal data leakage**: the
model should not use information that would only become available after
the prediction time. These columns remain in the raw data and in this
dictionary for documentation.

Other features should also be reviewed against the exact prediction
scenario before final modeling. In particular, confirm whether each
variable would genuinely be available at enrollment. Do not assume that
every feature is valid for an enrollment-time prediction merely because
it is present in the dataset.

## 6. Data preparation reminders

-   Preserve the original raw file and its source column names.
-   Keep the target `Target` separate from the input features.
-   Treat coded categories such as `Course`, `Application mode`,
    `Previous qualification`, and occupations as categorical labels
    unless a justified modeling decision says otherwise.
-   Use a train/test split before fitting preprocessing steps that learn
    from data.
-   Fit encoders, scalers, feature selectors, and other learned
    preprocessing only on the training data, then apply the fitted
    transformations to validation/test data.
-   Evaluate the three classes individually as well as overall; accuracy
    alone may hide weaker performance on less frequent classes.
-   This dictionary documents the supplied variable table. It does not
    establish that any feature causes dropout or guarantees a useful
    prediction.

## 7. Source

UCI Machine Learning Repository. **Predict Students' Dropout and
Academic Success.**

https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success
