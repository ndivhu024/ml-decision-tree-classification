# Machine Learning: Decision Tree Classification

## In this project I use supervised machine learning decision tree classification algorithm to develop a model that predict employees who are either at a risk of being terminated or quitting their job

### Problem set: Companies spend so much in the recrutting and training of new employees. The cost of continually training new recruits could be mitigated by identifying factors that help to retain employees.

### Data set: I use a synthetic HR data set (Source: Huebner & Patalano, 2019) to develop a model that predict who is at risk of either being terminated or leaving their job. If early indicators can be identified, the loss of valuable human resources could be prevented.

### Manage complexity of model: In order to avoid an overfitted model, I use cross-validation to find the optimum minimum leaf samples.This improved the accuracy score from 58.97% to 65.38%.

### Table 1: HR Data Set (Source: Huebner & Patalano, 2019). A list of variables used to develop my model, the response variable is Termd which indicates whether an employee has been terminated or not which is a categoical variable. The Type column is not on the original data set but I added it here for a quick check of Varible Types.

| Variable                 | Description                                                                                      | Type                 |
| ------------------------ | ------------------------------------------------------------------------------------------------ | -------------------- |
| *MarriedID*              | Is the employee married? (1 for yes, 0 for no)                                                   | Categorical (Binary) |
| *DeptID*                 | The department ID code from 1 to 6 that matches the department the employee works in             | Categorical          |
| *PerfScoreID*            | The performance score code that matches the employee’s most recent performance score             | Categorical          |
| *FromDiversityJobFairID* | Was the employee sourced from the diversity job fair? (1 for yes, 0 for no)                      | Categorical (Binary) |
| *PayRate*                | The employee’s hourly pay rate (all salaries are converted to hourly pay rate)                   | Numerical            |
| *Termd*                  | Has this employee been terminated? (1 for yes, 0 for no)                                         | Categorical (Binary) |
| *EmpSatisfaction*        | A basic satisfaction score between 1 and 5, as reported on a recent employee satisfaction survey | Numerical (Discrete) |
| *SpecialProjectsCount*   | The number of special projects that the employee worked on during the past 6 months              | Numerical (Discrete) |

### DeptID is an unordered categorical predictor, meaning there is no ordinal relation among its classes (1–6). To prevent the decision tree algorithm from treating it as an ordered variable, I apply One-Hot Encoding. This transforms DeptID into separate binary columns for each class, where 1 indicates membership in a particular class and 0 indicates absence. Table.2 and Table.3 below illustrate One-Hot Encoding.

### Table 2: DeptID

| Department |
|---|
| 1 |
| 2 |
| 3 |

### Table 3: One-Hot Encoded DeptID

| Department 1 | Department 2 | Department 3 |
|---|---|---|
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 0 | 0 | 1 |

