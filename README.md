# Student Performance Predictor

Implemented a research paper on predicting secondary school students' performance using regression and classification models of Machine Learning.

## Introduction
The research papers aims to find an approach to predict secondary school student's final grades based on past student grades, demographic, social and school related features. The dataset used for this project has data for 395 students in Mathematics.

## Data
For each student, below are the features -

- `school` - student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)
- `sex` - student's sex (binary: 'F' - female or 'M' - male)
- `age` - student's age (numeric: from 15 to 22)
- `address` - student's home address type (binary: 'U' - urban or 'R' - rural)
- `famsize` - family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3)
- `Pstatus` - parent's cohabitation status (binary: 'T' - living together or 'A' - apart)
- `Medu` - mother's education (numeric: 0 - none,  1 - primary education (4th grade), 2 â€“ 5th to 9th grade, 3 â€“ secondary education or 4 â€“ higher education)
- `Fedu` - father's education (numeric: 0 - none,  1 - primary education (4th grade), 2 â€“ 5th to 9th grade, 3 â€“ secondary education or 4 â€“ higher education)
- `Mjob` - mother's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
- `Fjob` - father's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
- `reason` - reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other')
- `guardian` - student's guardian (nominal: 'mother', 'father' or 'other')
- `traveltime` - home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30 min. to 1 hour, or 4 - >1 hour)
- `studytime` - weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10 hours, or 4 - >10 hours)
- `failures` - number of past class failures (numeric: n if 1<=n<3, else 4)
- `schoolsup` - extra educational support (binary: yes or no)
- `famsup` - family educational support (binary: yes or no)
- `paid` - extra paid classes within the course subject (Math or Portuguese) (binary: yes or no)
- `activities` - extra-curricular activities (binary: yes or no)
- `nursery` - attended nursery school (binary: yes or no)
- `higher` - wants to take higher education (binary: yes or no)
- `internet` - Internet access at home (binary: yes or no)
- `romantic` - with a romantic relationship (binary: yes or no)
- `famrel` - quality of family relationships (numeric: from 1 - very bad to 5 - excellent)
- `freetime` - free time after school (numeric: from 1 - very low to 5 - very high)
- `goout` - going out with friends (numeric: from 1 - very low to 5 - very high)
- `Dalc` - workday alcohol consumption (numeric: from 1 - very low to 5 - very high)
- `Walc` - weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)
- `health` - current health status (numeric: from 1 - very bad to 5 - very good)
- `absences` - number of school absences (numeric: from 0 to 93)
- `G1` - first period grade (numeric: from 0 to 20)
- `G2` - second period grade (numeric: from 0 to 20)
- `G3` - final grade (numeric: from 0 to 20, output target)

## Approach
Various demographic, social and school-related variables were correlated with past failures in terms of visuals, which helped to drill down to the factors contributing to maximum failures. To build a model to predict scores (using regression) and to classify if a student passed (using classification), various pre-processing steps were done using OrdinalEncoder & OneHotEncoder. Both both regression & classification, **Random Forest**, **SVM** & **Decision Trees** were used.

Out of 395 data points, 315 were considered for training & remaining 80 for testing.

For Set A, prediction was done using all input variables. For Set B, G1 was ignored and finally for Set C, both G1 & G2 were not considered as a part of model training.

## Results & Conclusion
My models validated the findings of the research paper - the model's maximum accuracy is when we have both G1, G2 in training data and predicting G3 becomes increasingly difficult as we keep dropping period grades. 

## Acknowledgements

https://archive.ics.uci.edu/dataset/320/student+performance

Using data mining to predict secondary school student performance (http://repositorium.sdum.uminho.pt/bitstream/1822/8024/1/student.pdf)
By P. Cortez, A. M. G. Silva. 2008
Published in Proceedings of 5th Annual Future Business Technology Conference
