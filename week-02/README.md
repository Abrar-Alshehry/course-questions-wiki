## Week 2 Quiz Questions and Answers

In order to prepare your Week 2 Quiz submission, please edit ***this*** document to provide substantive questions for each Quiz Problem and SAS Recipe listed below, as well as answers to at least three questions raised.

All edits should conform to GitHub Markdown specifications (https://guides.github.com/features/mastering-markdown/) and should be committed to a branch named "week-2" in your fork of this repo. Then, after all edits have been made/committed, your Week 2 Quiz should be submitted by initiating a pull request using

- the master branch of the stat6250/course_questions_wiki repo as the base fork and

- the week-2 branch of your version of the repo as the head fork.

The instructor will then review the pull request and make comments should further revision be needed. Then, after the contents of the pull request have been finalized without any merge conflicts, the instructor will merge the pull request.

********************************************************************************



[Course Textbook Chapter 1, Problem 1]
* *Question (aalshehry−stat6250):* Wht is themaximum number of observations per dataset? What about variables/columns?
- Question (lzhao4−stat6250): Do missing values affect the structure of the data set?
- Question (yren10−stat6250): When comparing two observations in one data set, if one observation missing 1 variable value, are we still able to do the comparison? Are we still getting a correct result?


[Course Textbook Chapter 1, Problem 2]
* *Question (aalshehry−stat6250):* Why should we use “run;” steatment many times within SAS program instead of one time at the end?
* *Answer (aalshehry−stat6250):* The "run;" statement is often not strictly required, as SAS will assume you want to start a new step when it sees data or proc. However your code will be clearer and easier to understand if you make the end of each step explicit.
- Question (lzhao4−stat6250): Add run statement after each program step is an essential?character variable is valid when contains letters and underscores.
- Question (yren10−stat6250): Can we usually use a single letter like "U" or “U.T” in stead "user.table"?


[Course Textbook Chapter 1, Problem 3]
* *Question (aalshehry−stat6250):* How many type of variables does SAS support?
- Question (lzhao4−stat6250): Can numeric variable contains letter and underscore?
- Answer (lzhao4−stat6250): A numeric variable can only contain numeric values. A 
- Question (yren10−stat6250): Does a variable named like "Account number" means it's has to be a numeric variable?
- Answer (yren10−stat6250): No, name can't decide the type.


[Course Textbook Chapter 1, Problem 4]
* *Question (aalshehry−stat6250):* How to represent missing data in SAS dataset?
- Question (lzhao4−stat6250): Can missing value indicates a different type of variable?
- Question (yren10−stat6250): Does a missing value in a variable column affects the type of the variable?
- Answer (yren10−stat6250): No, a blank dpesn't represent anything, the missing value is indcated by a period. 


[Course Textbook Chapter 1, Problem 5]
* *Question (aalshehry−stat6250):* Can a character variable begins with a number?
- Question (lzhao4−stat6250): What is the basic rule to set a valid variable name in SAS?
- Question (yren10−stat6250): Can a variable name contains other symbol like "$" or "#"?
- Answer (yren10−stat6250): No,can only contains numbers, letters or underscores.


[Course Textbook Chapter 1, Problem 8]
* *Question (aalshehry−stat6250):* Considering all numeric variables have a default length of 8 bytes, what is the maximum value that can SAS accept for a numeric variable?
* *Answer (aalshehry−stat6250):* 
![8 byte](https://github.com/aalshehry-stat6250/course-questions-wiki/blob/Week-2/week-02/8byte.JPG?raw=true)
- Question (lzhao4−stat6250): No matter a numeric variable contains how many digits it has a default length of 8?
- Answer (lzhao4−stat6250): Numeric variable balance always has a default length of 8 unless you set a specific length.
- Question (yren10−stat6250): If all numbers are integers, are they going to have different default length compare to non-integers?


[Course Textbook Chapter 2, Problem 3]
* *Question (aalshehry−stat6250):* Where and how to use YEARCUTOFF option?
- Question (lzhao4−stat6250):  YEARCUTOFF= option has no effect in some cases?
- Answer (lzhao4−stat6250): The YEARCUTOFF= option has no effect when processing dates with four-digits years, processing dates already stored as SAS date values, and displaying dates with SAS date formats.
- Question (yren10−stat6250): Does the date affect the value of YEARCUTOFF=option ?


[Course Textbook Chapter 2, Problem 7]
* *Question (aalshehry−stat6250):* How to save your dataset in the permanent library?
- Question (lzhao4−stat6250): How to correctly assign a SAS libref?
- Question (yren10−stat6250): Can a SAS engine access other format except SAS file format?


[Course Textbook Chapter 2, Problem 8]
* *Question (aalshehry−stat6250):* Without using the YEARCUTOFF= option, how would SAS interpret 11/11/20? Is it 1920 or 2020?
* *Answer (aalshehry−stat6250):* The default value of YEARCUTOFF= is 1920.
- Question (lzhao4−stat6250): How does YEARCUTOFF= option work on the interpretation of two-digits years?
- Question (yren10−stat6250): “YEARCUTOFF=” specifies 100-year span, what if we need a 200-year span or more?


[Course Textbook Chapter 2, Problem 9]
* *Question (aalshehry−stat6250):* If a SAS session is ended or a libref is deleted, does the library still exist?
* **Answer (aalshehry−stat6250): In these cases, SAS no longer has access to the files in the library.
- Question (lzhao4−stat6250): Libref exists only during the session in which it is created?
- Question (yren10−stat6250): What is the difference or relation between library and libref?


[basic_recipe_for_loading_data_from_remote_Excel_file (from Week 2 Overview)]
* *Question (aalshehry−stat6250):* Is it mandatory to use “filename tempfile clear;” step? Why?
- Question (lzhao−stat6250): Do we possible to transfer data from SAS dataset to an excel file? How? 
- Question (yren10−stat6250): Are we actually able to find the tempfile in our PC after all? 


[optional: bonus_advanced_recipe_for_loading_data_from_remote_Excel_file (from Week 2 Overview)]
