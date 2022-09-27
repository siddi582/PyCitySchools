# PyBer City School Analysis
 The following program was run using Anaconda, Jupyter Notebook, Pandas & Python
 ## Overview of Project
List of deliverables for the analysis:

A high-level snapshot of the district's key metrics, presented in a table format
An overview of the key metrics for each school, presented in a table format
Tables presenting each of the following metrics:
Schools, based on the overall passing rate
The average math score received by students in each grade level at each school
The average reading score received by students in each grade level at each school
School performance based on the budget per student
School performance based on the school size
School performance based on the type of school

**Before we can begin these tasks, we need to import the datasets into Jupyter Notebook using Python.

###Resources
Data Source: Student_Data_Challenge_Starter_Code.ipynb file and rename it Pyber_Analysis.ipynb.
Software: Python 3.9, Visual Studio Code 1.50.0, Anaconda 4.8.5, Jupyter Notebook 6.1.4, Pandas
For more information, read the Documentation on Pandas DataFrame.

#SUMMARY
Maria has gotten a new version of the student data with several changes. This includes an additional column: "school budget". She wants you to rework part of your analysis by using the new dataset.

#Deliverable 1: Collecting the Data

The path to the file is built by using os.path.join. (2 points)

The DataFrame is created and named student_df. (2 points)

The first five rows of data are displayed

#Deliverable 2: Prepare the Data (25 points)

In the student DataFrame, check for rows that have NaN (or missing) values, and remove those rows, as the following image shows:

A screenshot depicts each column name with a zero.
![data-4-challenge-2-1](https://user-images.githubusercontent.com/111712209/192464005-1e0156ec-93d6-4b4b-aa2c-06340a4debc2.png)


In the student DataFrame, we check for duplicate rows, and remove them.

We check for the data types of the columns by using the dtypes property, as the following image shows:
![dtypes](https://user-images.githubusercontent.com/111712209/192466073-089ed5bd-4631-4938-9f3a-b10cc526c728.png)

A screenshot depicts the name and type of each column. The "grade" column is of type object.

In the grade column, remove the "th" suffix from every value by using str and replace, as the following image shows:
![Str replace](https://user-images.githubusercontent.com/111712209/192466904-686d6acd-821b-4f4a-abf0-4d28228bcbd2.png)


A screenshot depicts the "grade" column without the "th" suffixes.

We changed the "grade" column to the int type, and then verify the column types, as the following image shows underneath the string:

![ChangingGrade](https://user-images.githubusercontent.com/111712209/192467741-92707f7b-0459-4226-8acd-66057e4bddff.png)


A screenshot depicts each column name and type. The "grade" column has a type of int64.

![GradeToInt](https://user-images.githubusercontent.com/111712209/192468110-d4eb9e2a-8ac5-4fff-88ee-6423fbc53b99.PNG)

#Deliverable 2 
After the removal of null values, we use isna().sum() displays 0 for all the columns. 
![Duplicates](https://user-images.githubusercontent.com/111712209/192468807-7548d0de-8e77-4fd9-a356-8daedc7ebd85.png)

After the removal of duplicates, duplicated().sum() displays no duplicates. 

The column types are displayed. 

The "th" suffix is removed from all the values in the "grade" column. 

The "grade" column is successfully converted to an int type. 
![GradeInt](https://user-images.githubusercontent.com/111712209/192469063-db948275-0cc6-4719-acf0-97e31501ee1b.png)

#Deliverable 3 : Summarize the Data
The summary statistics for the DataFrame are displayed

![SummaryStats](https://user-images.githubusercontent.com/111712209/192471024-ce54abbb-79e1-4441-bc8a-3035d1ee8663.png)

'Summary Stats'

The mean of the "math_score" column using the mean function is shown
![MeanScore](https://user-images.githubusercontent.com/111712209/192472452-f8909659-6be3-4e53-90e1-194b7c7d0f05.png)

"Mean"

The minimum of the "reading_score" column is stored in min_reading_score 
![MinScore](https://user-images.githubusercontent.com/111712209/192472753-887ca914-6d15-48ec-a801-db696dd93c00.png)

"Min_Reading_Score"

#Deliverable 4: Drill Down into the Data

The "grade column is displayed using loc
![LockOnGrade](https://user-images.githubusercontent.com/111712209/192473541-794f20e9-a777-4ac6-b397-f9fe20b26f71.png)

The first 3 rows of Columns 3, 4, 5 are displayed using iloc 
![iloctheGrades](https://user-images.githubusercontent.com/111712209/192473843-96ef4c92-e6f1-4489-ae75-454441d372ba.png)

The summary statistics for 9th graders are displayed
![Grade9ers](https://user-images.githubusercontent.com/111712209/192474074-262d5b04-3dd2-4995-b3bb-a6ec453588f8.png)

The row that contains the minimum reading score is displayed using loc and describe

![locAndDescribe()](https://user-images.githubusercontent.com/111712209/192475256-ba07c4b0-6db0-4449-ac4d-5453c75021c0.png)

The reading scores of the 10th graders at Dixon High School is displayed
![MinReadingScore](https://user-images.githubusercontent.com/111712209/192474384-d989113c-4bf0-485e-96f3-c5cbe988ea2b.png)

![ReadingScores](https://user-images.githubusercontent.com/111712209/192476324-103912af-1451-4477-bc8e-3a748945507f.png)

The average reading score of all the students in Grades 11 and 12 is combined and calculated 
![Gr11 12s](https://user-images.githubusercontent.com/111712209/192476495-0c77ce66-64cc-4548-9823-c6dfc2880db9.png)

Deliverable 5: Compare the Data
The average budget for each school type is displayed using groupby and mean functions as shown. 
![GroupbyMean](https://user-images.githubusercontent.com/111712209/192476933-d5d955dd-d6a0-4fb6-ac16-bec0cfbbcd0b.png)

The total number of students per school is displayed in descending order using groupby, count, sort_values. 
![Groupby](https://user-images.githubusercontent.com/111712209/192477480-c135673f-6f83-4f4c-a682-7eda13aad510.png)

"Groupby"

![count()](https://user-images.githubusercontent.com/111712209/192477768-d3459a93-9b9d-462c-be95-2ddba30751e5.png)

"Count"

![Sort_Values](https://user-images.githubusercontent.com/111712209/192478023-d277e46a-dbda-478d-af42-5e37b39ec099.png)

"sort_values"
The average math scores for each combination of grade and school type are displayed. 

Deliverable 6: Report Findings

An overview and understanding of the performed analysis 
While conducting this analysis, I made a few discoveries with the data between Charter type schools and public schools. Charter types have a higher performance score on a lower budget as opposed to public schools.
This could be a result of them allocating their resources carefully and investing in the right tools for student success. Also, as supported by the data, Charter types have a higher reading and math score. By looking at the data, while it is true that public schools have a higher budget overall, they also tend to have more students. This shows why publlic schools have varying data such as how grade 12s perform better in public school than the grade 12s at charter type schools as depicted 
