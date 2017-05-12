## Week 7 Quiz Questions and Answers

In order to prepare your Week 7 Quiz submission, please edit ***this*** document to provide substantive questions for each Quiz Problem and SAS Recipe listed below, as well as answers to at least three questions raised.

All edits should conform to GitHub Markdown specifications (https://guides.github.com/features/mastering-markdown/) and should be committed to a branch named "week-7" in your fork of this repo. Then, after all edits have been made/committed, your Week 7 Quiz should be submitted by initiating a pull request using

- the master branch of the stat6250/course_questions_wiki repo as the base fork and

- the week-7 branch of your version of the repo as the head fork.

The instructor will then review the pull request and make comments should further revision be needed. Then, after the contents of the pull request have been finalized without any merge conflicts, the instructor will merge the pull request.

********************************************************************************



[Course Textbook Chapter 10, Problem 2]
- Question (mcardoso3-stat6250):  Does the 'Amount' label cover only numeric variables?
- Question (akumar30−stat6250): Does any variable formatted in the PROC PRINT output statement override the same variable formatted in DATA step?
- Answer (akumar30−stat6250):  Yes, any format option that are done in a PROC PRINT step supersede the data step format assignments for same variable.
* *Question (aalshehry−stat6250):* How to assign the formats permanently?  
* *Answer (aalshehry−stat6250):*  Formats can be assigned temporarily in PROC steps and permanently in DATA steps.
- Question (kveng−stat6250): What is COMMA10 format?
- *Question* (lwang30-stat6250) : Can we take the label and format statement in the data step away as they will be overwritten by "proc print" anyway ?
- Question (lzhao4-stat6250): Can temporary labels which assigned in a PROC step override the permanent labels which assigned in a Data step?
- Question (dlee117−stat6250): What is the difference between COMMA6 and COMMA10?



[Course Textbook Chapter 10, Problem 6]
- Question (mcardoso3-stat6250):  How many different ways are there of writing an IF-THEN statement in SAS?
- Question (akumar30−stat6250): What is the order of execution in case of multiple IF-THEN statement?
- Answer (akumar30−stat6250):  Each IF statement is evaluated in order it define, even if the first condition is true. 
* *Question (aalshehry−stat6250):* When we use IF-THEN statement, how to differenciate between variable type?
- Question (kveng−stat6250): How does Count+1 work?
- Answer (kveng−stat6250): The count+1 statement creates the variable count and adds one to each oservation as SAS processes the data step.
- *Question* (lwang30-stat6250) : What types of variable are present in this problem ?
- Question (lzhao4−stat6250): What need attention when identify character values in an IF-THEN statement? 
- Answer (lzhao4-stat6250): In IF-THEN statement, you need to enclose character values in quotation mark, and specify them in same case how they exactly appear in the data set. 
- Question (dlee117−stat6250): For Chapter 10 Quiz, problem 6, if both if statements were false, what would be the values of the variables Count and Control?
- Answer (dlee117-stat6250): The value of Count would be 12 and the value of Control would be Go.



[Course Textbook Chapter 10, Problem 7]
- Question (mcardoso3-stat6250):  How long can a new variable be by using the LENGTH statement?
- Question (akumar30−stat6250): What happen if LENGTH statement appears after any other reference to the variable in the DATA step?
- Answer (akumar30−stat6250):  If the variable has been created by another statement, then a later use of the LENGTH statement will not change its length.
* *Question (aalshehry−stat6250):* Why we might want to specify a length for a character variable, rather than let the first assigned value determine the length?
- Question (kveng−stat6250): What is LENGTH statement?
- Answer (kveng−stat6250): You can use a LENGTH statement to specify a length (the number of bytes) for a variable before the first value is referenced elsewhere in the DATA step. For example: LENGTH Type $ 8;
- *Question* (lwang30-stat6250) : What is the consequence of the subsequent observations having longer values than the first observation without the length of the variable being specified in the statement ?
- *Answer* (lwang30-stat6250) : All subsequent values are truncated to the same length as the first observation's value.
- Question (lzhao4−stat6250): How to specify length for variables?
- Question (dlee117−stat6250): What does it mean when a value is truncated?
- Answer (dlee117-stat6250): It means if the value is longer than the assigned length, the value is shortened to the assigned length. 



[Course Textbook Chapter 10, Problem 8]
- Question (mcardoso3-stat6250):  What is the benefit of using ELSE in an IF-THEN statement?
- Answer (mcardoso3-stat6250):  In a IF-THEN statement with ELSE, SAS executes IF-THEN statements until it encounters the first true statment.
- Question (akumar30−stat6250): Which one has better performance in SAS, multiple if then statement or nested if else statement?
* *Question (aalshehry−stat6250):* What is the benifit of using ELSE in IF-THEN statement?
* *Answer (aalshehry−stat6250):* SAS wont evaluate the code that included within ELSE statement unless all previous IF's are not meet the condition which can save some resources.
- Question (kveng−stat6250): Can we write multiple ELSE statements to specify a series of mutally exclusive conditions?
- Answer (kveng−stat6250): Yes, the ELSE statement must immediately follow the IF-THEN statement in your program.
- *Question* (lwang30-stat6250) : What is the advantage of using the IF-THEN/ELSE statement ?
- *Answer* (lwang30-stat6250) : When the dataset is large, IF-THEN/ELSE statement can process much faster than multiple IF-THEN statement in which all the observations are evaluated one by one.
- Question (lzhao4−stat6250): How to use ELSE statements with the IF-THEN statement?
- Answer (lzhao4-stat6250): You should write ELSE statement immediately follow the IF-THEN statement. Additionally, you can use multiple ELSE statements when needed.  
- Question (dlee117−stat6250): Why is it more efficient to construct IF-THEN/ELSE statements with conditions of decreasing probability?



[Course Textbook Chapter 10, Problem 9]
- Question (mcardoso3-stat6250):  Is there a limit to including how many LENGTH statements you type in SAS?
- Question (akumar30−stat6250): What is the ideal position to define the length statement so that the program can run successfully?
- Answer (akumar30−stat6250):  The LENGTH statement should appears before any other reference to the variable in the DATA step.
* *Question (aalshehry−stat6250):* In case of using LENGTH statement to assign a length to a character variable, where it supposed to be located?
* *Answer (aalshehry−stat6250):* It must be the first reference to the character variables in the DATA step. Therefore, the best position in the DATA step for a LENGTH statement is immediately after the DATA statement.
- Question (kveng-stat6250): In which order should the LENGTH statement appears in the DATA step?
- *Question* (lwang30-stat6250) : Where should we place the LENGTH statement in order to let variable "Type" have a length of 10 ?
- Question (lzhao4−stat6250): Does LENGTH statement can change the length of an existing variable?
- Question (dlee117−stat6250): Can you specify a new LENGTH of a variable after the first value for the variable is referenced?



[Course Textbook Chapter 10, Problem 10]
- Question (mcardoso3-stat6250):  What are the possible errors that you can commit while writing a LENGTH, INFILE, or IF-THEN statement?
- Question (akumar30−stat6250): Can we create a new calculated variable in data step which doesn’t exists in keep statement?
* *Question (aalshehry−stat6250):* What are the  differences between the DROP & KEEP statements and the DROP= & KEEP= data set options?
- Question (kveng−stat6250): Can we drop or keep variables in the PROC steps?
- *Question* (lwang30-stat6250) : What is the difference between the "DROP or KEEP" statement and the "DROP= or KEEP=" statement ?
- Question (lzhao4−stat6250): What’s the difference between DROP statement and DROP= data set option? 
- Question (dlee117−stat6250): Do you have to provide a label and format for a variable?



[Course Textbook Chapter 11, Problem 1]
- Question (mcardoso3-stat6250):  Is it required to have both the DROP and KEEP data set options within the same statement?
- Answer (mcardoso3-stat6250):  If certain variables are not referenced, you can use the DROP= option in the SET statement, which doesn't require yo to use the KEEP= option.
- Question (akumar30−stat6250): Does drop statement delete the variables from its original dataset?
* *Question (aalshehry−stat6250):* If you use more than one data set option or a combination of data set options and statements, what is the order that SAS applying for drops, keeps, and renames variables?
- Question (kveng−stat6250): How does KEEP=option in the SET statement work?
- *Question* (lwang30-stat6250) : What are the statements where we can use the "DROP= or KEEP=" option ?
- Question (lzhao4−stat6250): Where to specify the KEEP= data set option?
- Question (dlee117−stat6250): What is the difference between using DROP= and KEEP= statements in the DATA step vs the SET step?



[Course Textbook Chapter 11, Problem 2]
- Question (mcardoso3-stat6250):  Will the new data set being created always come before the previous data set has ben specified?
- Question (akumar30−stat6250):  Can Data and set option have same dataset name to override the existing dataset?
* Question (aalshehry−stat6250): What kind of IF logical operators can we use within a DATA step?
- Question (kveng−stat6250): Can we drop ordertime from the SET statement in this case?
- *Question* (lwang30-stat6250) : What is the basic criterion to be based on in order to figure out the correct place where the "DROP= or KEEP=" option should be located ? 
- Question (lzhao4−stat6250): Where to specify the DROP= data set option? 
- Question (dlee117−stat6250): What does “july” mean when referencing the data set Orders with this statement: july.orders?



[Course Textbook Chapter 11, Problem 3]
- Question (mcardoso3-stat6250):  Why is there no 'middle' variable in each BY group?
- Question (akumar30−stat6250): Can we specify multiple variables together in BY statement for multiple group observations for processing at same time?
* *Question (aalshehry−stat6250):* Can we use multiple BY statements within a DATA step?  
* *Answer (aalshehry−stat6250):* Only one BY statement can accompany each SET statement in a DATA step.
- Question (kveng−stat6250): Where does the FRIST and LAST temporary varaibles are stored?
- *Question* (lwang30-stat6250) : What are the values of each FIRST. and LAST. when the BY-Group processing is used for multiple variables ?
- Question (lzhao4−stat6250): When using the BY statement with the SET statement, does the data step creates two temporary variables for each BY variable?
- Answer (lzhao4-stat6250): Yes, one is the named FIRST.VARIABLE and another is named LAST.VARIABLE. They are identifying the first and the last observation in each BY group.
- Question (dlee117−stat6250): What are the values in FIRST.variable and LAST.variable?
- Answer (dlee117-stat6250): Their values are either 1 for the first and last observations respectively or 0 for any other observation.



[Course Textbook Chapter 11, Problem 8]
- Question (mcardoso3-stat6250):  How would continous looping happen when submitting a program?
- Answer (mcardoso3-stat6250):  The POINT= option reads only specified observations, so SAS can't read an end-of-file indicator as it would if the file was read sequentially.
- Question (akumar30−stat6250): What is the major difference between END=options and POINT= options statement?
* *Question (aalshehry−stat6250):* What is the value of the END= variable when random access is used?
- Question (kveng−stat6250): What does "if last" referred to in this statement?
- *Question* (lwang30-stat6250) : In what situations do we want to use the END= option to manipulate the data ?
- Question (lzhao4−stat6250): When to use an END= option in the SET statement?
- Question (dlee117−stat6250): Is “LAST” a SAS defined statement or is it a variable?



[Course Textbook Chapter 11, Problem 9]
- Question (mcardoso3-stat6250):  How soon would observations be revealed when the DATA step has been executed?
- Question (akumar30−stat6250):  What is the content of program data vector after compilation phase is completed of data step?
- Answer (akumar30−stat6250):  The descriptor portion of the new SAS Data set is created after compilation phase of data step is complete. There are no observations because the DATA step has not yet executed.
* *Question (aalshehry−stat6250):* What are the added values of using program data vector (PDV) compared to the other database platforms?
- Question (kveng−stat6250): What is program data vector (PDV)?
- *Question* (lwang30-stat6250) : What are the values of each variable in the PDV at the beginning of the execution phase ?
- *Answer* (lwang30-stat6250) : The values of each variable are set to missing at the beginning of the execution phase.
- Question (lzhao4−stat6250): In compilation phase, how SAS reading an existing data set with the SET statement?
- Question (dlee117−stat6250): If variables are created in the DATA step, what happens to them during the compilation phase?



[basic_recipe_for_combining_data_vertically (from Week 7 Overview)]
- Question (mcardoso3-stat6250):  Why would a length statement need to appear when creating wider character variable?
- Question (akumar30−stat6250): If there are two data set having same data structure but variable names and position are different? Can we combine this dataset vertically by using additional keep and retain statement?
* *Question (aalshehry−stat6250):* What is the main advantage of using "IN=" Statement?
- Question (kveng−stat6250): When combining the data vertically, can we sort and combine the data at the same time?
- *Question* (lwang30-stat6250) : What is an example of the expansion of the dataset by applying both two indicator variables that has been defined in the "set" statement ?
- Question (lzhao4−stat6250): From the recipe we know that IN= dataset option can be used in conjunction with if or else conditioning. Beside this, what else we can do with IN= dataset option?
- Question (dlee117−stat6250): What is the function of the SAS statement DO?



[optional: adv_recipe_for_combining_data_vertically (from Week 7 Overview)]
- Question (mcardoso3-stat6250):  What would be the best option to combine datasets in SAS?
- Question (akumar30−stat6250): How to rewrite concat statement using pro sql?
- Answer (akumar30−stat6250):  The two data sets can be combined vertically, or concatenated, in a DATA step by naming them both in a single SET statement. Here is the example where two dataset 'one' and 'two' are being concatenated:
```SAS
DATA concat; 
SET one two; 
RUN;
*The equivalent SQL statement of concatenated is;
CREATE TABLE concat AS
SELECT *
FROM one
OUTER UNION CORRESPONDING
SELECT *
FROM two
;
```
* *Question (aalshehry−stat6250):* How to sort the selected data using PROQ SQL?
- *Question* (lwang30-stat6250) : What are the advantages and disadvantages of using "proc sql" rather than a data step ?


