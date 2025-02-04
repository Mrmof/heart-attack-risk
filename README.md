# heart-attack-risk
Objective of the Analysis
This analysis is intended to provide an overview of the risk of heart attack of various age groups as well as cholesterol and liproprotein levels. The study also provides a predictive model for determining the likelihood of heart attacks.


Questions
1. What is the average distribution for total cholesterol, heart heart and diabetes levels across various age grades? 
2. What is the relationship between Total Cholesterol and Heart Attack?
3. How does LDL and HDL infleunce Total cholesterol levels?
4. Determines if high cholesterol levels increase heart attack risk?
5. Generate the predictive model to determine likelihood of developing a heart attack?

Data Collection and Description
The dataset was obtained from https://www.kaggle.com/datasets/shriyashjagtap/heart-attack-risk-assessment-dataset. the dataset consist of 10 columns and 1000 rows.

Data Transformation
The obtained csv file was imported into excel using the powerquery wizard and analyzed.
The columns were assessed and set to appropriate data types.
A new column "Gender" was created grading 1 as male and 0 as female using power query (= if [sex] = 1 then "Male" else "Female") and the dataset was loaded into ms excel.
The dataset was evaluated to remove outliers for the age column by evaluating lower and upper boundary.
first quartile =QUARTILE.INC(updated_version[age],1)
third quartile =QUARTILE.INC(updated_version[age],3)
InterQuartile =O3-O2
Lower bound =O2-(1.5*O4)
Upper bound =O3+(1.5*O4) 
=IF([@age]<$O$6, "Wrong", IF([@age]>$O$7, "Wrong", "Correct"))
