## Week 6 Quiz Questions and Answers

In order to prepare your Week 6 Quiz submission, please edit ***this*** document to provide substantive questions for each Quiz Problem and SAS Recipe listed below, as well as answers to at least three questions raised.

All edits should conform to GitHub Markdown specifications (https://guides.github.com/features/mastering-markdown/) and should be committed to a branch named "week-6" in your fork of this repo. Then, after all edits have been made/committed, your Week 6 Quiz should be submitted by initiating a pull request using

- the master branch of the stat6250/course_questions_wiki repo as the base fork and

- the week-6 branch of your version of the repo as the head fork.

The instructor will then review the pull request and make comments should further revision be needed. Then, after the contents of the pull request have been finalized without any merge conflicts, the instructor will merge the pull request.

********************************************************************************



[Course Textbook Chapter 12, Problem 1]
* *Question (aalshehry−stat6250):* What is the right way to concatenate two datasets in a new one?
* *Answer (aalshehry−stat6250):* By using the following syntax: 
```SAS
DATA SAS-data-set;
       SET SAS-data-set1 SAS-data-set2 ...;
RUN;
```
- Question (akumar30−stat6250): Is the order of the smallest dataset significance in one-to-one merge SET data statement? 
- Question (yzhu12-stat6250): Why there is no end-of-file condition when you use direct access?
- Question (meisenbach-stat6250): When would you use this one-to-one merging?
- Answer (meisenbach-stat6250): When the observations in both datasets are in the same order and the columns are different.
- Question (lzhao4-stat6250): How does SAS reading values when same named variables occur?
- Question (kveng-stat6250): What are the methods of combining data set?
- Answer (kveng-stat6250): There are one-to-one reading (statement: SET), concatenating (statement: SET), interleaving (statement: SET, BY), and match-merging (statement: MERGE, BY)



[Course Textbook Chapter 12, Problem 2]
* *Question (aalshehry−stat6250):* What is the main difference between using SET and Merge statements in DATA step?
- Question (akumar30−stat6250): How to append two dataset, when common variable has different type of data?
- Answer (akumar30−stat6250):  If the type of a variable in the DATA= data set is different than in the BASE= data set, SAS replaces all values for the variable in the DATA= data set with missing values and keeps the variable type of the variable specified in the BASE= data set
- Question (yzhu12-stat6250): What steps you must take to prevent continuous looping while using direct access to read data?
- Answer (yzhu12-stat6250): You either add a STOP statement to the DATA step, or use programming logic that checks for an invalid value of the POINT= variable.
- Question (meisenbach-stat6250): What is the benefit of using interleaving?
- Answer (meisenbach-stat6250): The output dataset is sorted by the BY variable.
- Question (lzhao4−stat6250): How to use BY statement and SET statement when interleave data sets?
- Question (kveng-stat6250): Can we use interleaving without changing the order?
- Answer (kveng-stat6250):  If we don't want to change the order, then we need to use concatenating method. It'll just concate multiple tables without sorting.



[Course Textbook Chapter 12, Problem 3]
* *Question (aalshehry−stat6250):* What is the default oreder of the output obsevations when SET statement is used to combine two datasets?
- Question (akumar30−stat6250): What happen when if the type of common variable differ in the datasets to be concatenated?
- Answer (akumar30−stat6250):  SAS will stops process the DATA step and issues an error message stating that the variables are incompatible.
- Question (yzhu12-stat6250): How do we determine when the last observation in an input data set has been read?
- Answer (yzhu12-stat6250): We use the END= option in the SET statement.
- Question (meisenbach-stat6250): With concatenate, what happens when rows have the same values for a particular variable (e.g. ID)?
- Answer (meisenbach-stat6250): Nothing, both rows are in the output.
- Question (lzhao4−stat6250): How will the output data set display when concatenate one date set to another?
- Question (kveng-stat6250): Which method does this problem invoke?
- Answer (kveng-stat6250): This problem invokes the concatenating method.



[Course Textbook Chapter 12, Problem 4]
* *Question (aalshehry−stat6250):* Before concatenate datasets, what should we pay attention to?
* *Answer (aalshehry−stat6250):*  It is important to know the structure and contents of the input datasets by checking the describtive part and the data as well.
- Question (akumar30−stat6250):  Can we concatenate more than two data set in SAS using single SAS concatenate procedure?
- Question (yzhu12-stat6250): How do you select the variables that you want to drop or keep?
- Answer (yzhu12-stat6250): You can use the DROP= and KEEP= data set options in parentheses after a SAS data set name.
- Question (meisenbach-stat6250): When should you use concatenate?
- Answer (meisenbach-stat6250): When both datasets essentially have the same columns and the missing columns are non-essential.
- Question (lzhao4−stat6250): What’s the difference between concatenate multiple data sets and merge multiple data sets?
- Question (kveng-stat6250): Is concatenating the best method to use in this case?



[Course Textbook Chapter 12, Problem 5]
* *Question (aalshehry−stat6250):* What is the best way to combine multiple datasets which have a primar-key variable?
- Question (akumar30−stat6250): Can we merge the two datasets with multiple common variables in single SAS Procedure by specifying multiple variable names in BY statement?
- Question (yzhu12-stat6250): When we read a single data set, which command do we use to specify the data set to be read?
- Answer (yzhu12-stat6250): We use SET statement.
- Question (meisenbach-stat6250): When two datasets have the same variable, how is the length of the variable determined?
- Answer (meisenbach-stat6250): The length is determined by the first dataset.
- Question (lzhao4−stat6250): How will the output data set display when couple variables with the same name are in more than one input data set?
- Answer (lzhao4-stat6250): Values of the same-named variable in the first data set in which it appears are overwritten by values of the same-named variable in subsequent data sets.
- Question (kveng-stat6250): When merging two tables with the same column label, can we specify which table to overwrite?



[Course Textbook Chapter 12, Problem 7]
* *Question (aalshehry−stat6250):* In MERGE statement, what the possible values for IN option? and how it can be utilized?
* *Answer (aalshehry−stat6250):*  The IN= variables have two possible values: 0 and 1 which indicates whether a data set contributed information to the observation: MERGE SAS-data-set1 <(IN=variable)>...
- Question (akumar30−stat6250): How do you prevent the values of the common variable Blue from being overwritten when you merge the two data sets?
- Answer (akumar30−stat6250):  Using RENAME procedure, we can change the name of common variables to sustain its original value from both dataset and prevent overwriting,
- Question (yzhu12-stat6250): What's the other programming features for manipulation data sets that the DATA step can provide?
- Answer (yzhu12-stat6250): We can use IF-THEN/ELSE logic with DO groups and DO loops to control processing that is based on one or more conditions, specify additional data set options, process variables in arrays and use SAS functions.
- Question (meisenbach-stat6250): When two datasets have the same variable, how do you keep just the values from the first dataset?
- Question (lzhao4−stat6250): How to prevent overwriting when merging variables which have same names. 
- Answer (lzhao4−stat6250): Can use RENAME= option to rename data set. 
- Question (kveng-stat6250): Can we change the column name with concatening and interleaving and match-merging method?



[Course Textbook Chapter 12, Problem 9]
* *Question (aalshehry−stat6250):* What will happen if two datasets were combined with the same variable name but with different type?
- Question (akumar30−stat6250): Can I get the result of one-to-one merge using PROC SQL command?
- Question (yzhu12-stat6250): What's the BY statement in SAS for?
- Question (meisenbach-stat6250): In a match-merge, how do you exclude records with missing values?
- Answer (meisenbach-stat6250): use the IN= data set option and an IF statement.
- Question (lzhao4−stat6250): How will the output data set display when merging multiple data sets without make any change of BY variable value retain the same? 
- Answer (lzhao4-stat6250): The value will retain from the previous observation to new data set. 
- Question (kveng-stat6250): Can we merge two columns together like first name and last name instead of merging the tables?



[basic_recipe_for_combining_data_horizontally (from Week 6 Overview)]
* *Question (aalshehry−stat6250):* Using Program Data Vector (PDV) has many advantages, but what are its disadvantages?
- Question (akumar30−stat6250):  Does rename option in merge statement modify the name of actual dataset or only valid for merge statement?
- Question (yzhu12-stat6250): For example, if we have a data set containing missing variables, how does the SAS combine the data sets horizontally and correctly, which means that the corresponding variables are sorted  and then combined horizontally?
- Question (meisenbach-stat6250): Why does the column name not also change when we use rename? Why does renaming the column name to a space result in the desired column name?
- Question (lzhao4−stat6250): When labels are assigned in the data set, are they available for all procedures use in that data set?
- Question (kveng-stat6250): Can we just merge without including retain and keep and label statements? 



[optional: adv_recipe_for_combining_data_horizontally (from Week 6 Overview)]
- Question (akumar30−stat6250): Wwhich statement will have faster performance combine four dataset, using merge statement or proc sql statement?
- Question (yzhu12-stat6250): What kind of error will occur if the order of these AS statements are converted improperly?
- Question (kveng-stat6250): What is coalesce? What does it do?


