# Student Performance Analysis

## Project Overview

This project performs exploratory data analysis (EDA) on a student
performance dataset using Python.

The main goal of this project is to clean the dataset, explore
student academic performance and identify relationships between
study habits, attendance and academic scores.

The project demonstrates a complete beginner-level data analysis
workflow using Pandas, NumPy and Matplotlib.

---

## Objectives

The main objectives of this project are:

- Inspect the dataset
- Identify and handle missing values
- Detect and correct invalid numerical values
- Identify and remove duplicate student records
- Standardize categorical data
- Analyze student performance
- Compare performance across subjects, classes and genders
- Identify the top-performing students
- Analyze average assessment scores
- Study the relationship between study hours and overall score
- Study the relationship between attendance and overall score
- Visualize important findings

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

## Dataset

The dataset contains student academic performance information.

### Dataset Columns

| Column | Description |
|---|---|
| Student ID | Unique identifier for each student |
| Student Name | Student name |
| Gender | Student gender |
| Class | Student class |
| Subject | Academic subject |
| Study Hours | Number of study hours |
| Attendance % | Student attendance percentage |
| Assignment Score | Assignment score |
| Midterm Score | Midterm examination score |
| Final Exam Score | Final examination score |
| Overall Score | Overall academic score |

---

## Data Cleaning

Several data cleaning steps were performed before analysis.

### 1. Removed Empty Rows

Completely empty rows were identified and removed from the dataset.

### 2. Handled Missing Values

Missing categorical values were replaced with:

`Unknown`

Missing numerical values were filled using the median of
the respective column.

### 3. Corrected Invalid Values

Invalid numerical values were identified using reasonable ranges.

Examples included:

- Negative study hours
- Study hours above 24
- Attendance below 0%
- Attendance above 100%
- Exam scores below 0
- Exam scores above 100

Invalid values were replaced with missing values and then
filled using the median.

### 4. Standardized Subject Names

Subject names were standardized to avoid duplicate categories
caused by differences in capitalization and spacing.

For example:

- `math`
- `Mathematics`

were standardized to:

`Mathematics`

### 5. Standardized Class Values

Class values were cleaned to remove unnecessary spaces and
inconsistent capitalization.

### 6. Standardized Gender Values

Gender values were standardized so that variations such as:

- `Male`
- `male`
- ` Male`

were treated as:

`Male`

Similarly, female values were standardized to:

`Female`

### 7. Removed Duplicate Student Records

Duplicate Student IDs were identified and duplicate records
were removed.

The final dataset contains:

**150 unique students**

---

## Exploratory Data Analysis

The following analyses were performed.

### Subject Performance

Average Overall Score by subject:

| Subject | Average Overall Score |
|---|---:|
| Computer Science | 75.54 |
| English | 75.51 |
| Physics | 74.48 |
| Mathematics | 74.33 |
| Chemistry | 70.94 |

Computer Science had the highest average Overall Score,
while Chemistry had the lowest.

---

### Class Performance

Average Overall Score by class:

| Class | Average Overall Score |
|---|---:|
| 10th | 77.55 |
| 9th | 74.20 |
| 11th | 73.47 |
| 12th | 72.15 |

The 10th class had the highest average Overall Score among
the known classes.

---

### Gender Performance

Average Overall Score by gender:

| Gender | Average Overall Score |
|---|---:|
| Male | 74.75 |
| Female | 74.12 |
| Unknown | 59.67 |

Male and female students had very similar average Overall Scores.
The Unknown category represents only a small number of records
and should not be used for a meaningful gender comparison.

---

### Assessment Performance

Average score for each assessment:

| Assessment | Average Score |
|---|---:|
| Assignment | 70.09 |
| Midterm | 78.44 |
| Final Exam | 70.76 |
| Overall | 74.15 |

The Midterm had the highest average score, while the Assignment
had the lowest average score.

---

## Top 10 Students

The top-performing students based on Overall Score were:

| Student ID | Student Name | Subject | Class | Overall Score |
|---|---|---|---|---:|
| STU144 | Student 144 | Physics | 12th | 100.0 |
| STU013 | Student 013 | Physics | 12th | 100.0 |
| STU003 | STUDENT 003 | English | 9th | 96.1 |
| STU027 | Student 027 | Physics | 9th | 96.0 |
| STU018 | Student 018 | English | 9th | 95.7 |
| STU044 | Student 044 | Mathematics | 10th | 95.7 |
| STU050 | Student 050 | Chemistry | 11th | 95.6 |
| STU002 | STUDENT 002 | Computer Science | 10th | 95.2 |
| STU040 | Student 040 | Mathematics | 9th | 94.5 |
| STU061 | Student 061 | Chemistry | 11th | 93.9 |

The highest Overall Score was 100, achieved by two students.

---

## Correlation Analysis

### Study Hours vs Overall Score

Correlation:

**0.785**

This indicates a strong positive relationship between Study Hours
and Overall Score.

Students who studied more hours generally tended to have higher
Overall Scores in this dataset.

### Attendance vs Overall Score

Correlation:

**0.461**

This indicates a moderate positive relationship between Attendance
and Overall Score.

Students with higher attendance generally tended to have higher
Overall Scores, although the relationship was weaker than the
relationship between Study Hours and Overall Score.

> Correlation indicates a relationship between variables and does
> not prove that one variable causes the other.

---

## Key Findings

The main findings from the analysis are:

1. The final dataset contains 150 unique students.
2. The overall average score is 74.15.
3. Computer Science had the highest subject average at 75.54.
4. Chemistry had the lowest subject average at 70.94.
5. 10th class had the highest average score at 77.55.
6. The Midterm had the highest average assessment score at 78.44.
7. The highest Overall Score was 100.
8. Study Hours had a strong positive correlation with Overall Score
   with a correlation of 0.785.
9. Attendance had a moderate positive correlation with Overall Score
   with a correlation of 0.461.
10. Male and female students had very similar average Overall Scores.

---

## Visualizations

The project includes visualizations for:

- Average Overall Score by Subject
- Average Overall Score by Class
- Average Overall Score by Gender
- Average Scores by Assessment
- Top 10 Students
- Study Hours vs Overall Score
- Attendance vs Overall Score

---

## Project Structure

```text
student-performance-analysis/
│
├── data/
│   ├── student_performance_raw_150.csv
│   └── student_performance_cleaned.csv
│
├── notebooks/
│   └── student_performance_analysis.ipynb
│
├── charts/
│   ├── subject_performance.png
│   ├── class_performance.png
│   ├── gender_performance.png
│   ├── study_hours_vs_overall.png
│   ├── attendance_vs_overall.png
│   ├── assessment_averages.png
│   └── top_10_students.png
│
├── README.md
├── requirements.txt
└── .gitignore


How to Run the Project

1. Clone the repository
git clone YOUR_GITHUB_REPOSITORY_URL

2. Navigate to the project directory
cd student-performance-analysis

3. Install the required libraries
pip install -r requirements.txt

4. Start Jupyter Notebook
jupyter notebook

5. Open the notebook

Open:

notebooks/student_performance_analysis.ipynb

Run the notebook cells from top to bottom.

Conclusion

This project demonstrates the basic workflow of exploratory data
analysis using Python.

The dataset was cleaned and standardized before analysis. Different
aspects of student performance were then explored using descriptive
statistics, grouping, sorting, correlation analysis and data
visualization.

One of the strongest findings was the positive relationship between
Study Hours and Overall Score, which had a correlation of 0.785.
Attendance also showed a positive relationship with Overall Score,
with a correlation of 0.461.

This project provides a foundation for further analysis and can be
extended into a machine learning project for predicting student
performance.

Author

Ali Hassan | Software Engineer

License

This project is for educational and portfolio purposes.