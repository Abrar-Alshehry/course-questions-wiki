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
- Question (dlee117−stat6250): In the given data set, what is considered an observation and what is considered a variable?
- Answer (dlee117-stat6250): An observation is a single row (Picker, M, 32) and a variable is a single column (Name).
- Question (yzhu12-stat6250): In a SAS table, what does the rows and columns represent?
- Answer (yzhu12-stat6250): The number of the rows represents observations, the number of the columns represents the variables.



[Course Textbook Chapter 1, Problem 2]
* *Question (aalshehry−stat6250):* Why should we use “run;” steatment many times within SAS program instead of one time at the end?
* *Answer (aalshehry−stat6250):* The "run;" statement is often not strictly required, as SAS will assume you want to start a new step when it sees data or proc. However your code will be clearer and easier to understand if you make the end of each step explicit.
- Question (lzhao4−stat6250): Add run statement after each program step is an essential?character variable is valid when contains letters and underscores.
- Question (dlee117−stat6250): When running the given program, is it ok that some of the lines in the code are indented?
- Answer (dlee117-stat6250): Yes, SAS statements are free-format. This means that they can begin and end anywhere on a line.
- Question (yzhu12-stat6250): What kind of statement in SAS represent executing previous steps in the program?
- Answer (yzhu12-stat6250): data, proc or run statement.



[Course Textbook Chapter 1, Problem 3]
* *Question (aalshehry−stat6250):* How many type of variables does SAS support?
- Question (lzhao4−stat6250): Can numeric variable contains letter and underscore?
- Answer (lzhao4−stat6250): A numeric variable can only contain numeric values. A 
- Question (dlee117−stat6250): Is it valid for the variable AcctNum to contain both numbers and letters?
- Question (yzhu12-stat6250): What's the difference between character variable and numeric variable?
- Answer (yzhu12-stat6250): character variables can contain any values while numeric variables can contain only numeric values. 



[Course Textbook Chapter 1, Problem 4]
* *Question (aalshehry−stat6250):* How to represent missing data in SAS dataset?
- Question (lzhao4−stat6250): Can missing value indicates a different type of variable?
- Question (dlee117−stat6250): Is it valid to change the variable name Brand to 10Brand? 
- Answer (dlee117-stat6250): No, each variable name has to begin with a letter or an underscore, not a number.
- Question (yzhu12-stat6250): If a data value is unknown for a particular observation, where should we find the missing value?
- Answer (yzhu12-stat6250): The missing value is recorded in the SAS data set automatically.



[Course Textbook Chapter 1, Problem 5]
* *Question (aalshehry−stat6250):* Can a character variable begins with a number?
- Question (lzhao4−stat6250): What is the basic rule to set a valid variable name in SAS?
- Question (dlee117−stat6250): Can variable names contain a space?
- Question (yzhu12-stat6250): Is the variable name @Bunny01 a valid name? 
- Answer (yzhu12-stat6250): No, it's not a valid name because it must begin with a letter (A–Z, either uppercase or lowercase) or an underscore, and can continue with any combination of numbers, letters, or underscores. 



[Course Textbook Chapter 1, Problem 8]
* *Question (aalshehry−stat6250):* Considering all numeric variables have a default length of 8 bytes, what is the maximum value that can SAS accept for a numeric variable?
* *Answer (aalshehry−stat6250):* 
![8 byte](https://github.com/aalshehry-stat6250/course-questions-wiki/blob/Week-2/week-02/8byte.JPG?raw=true)
- Question (lzhao4−stat6250): No matter a numeric variable contains how many digits it has a default length of 8?
- Answer (lzhao4−stat6250): Numeric variable balance always has a default length of 8 unless you set a specific length.
- Question (dlee117−stat6250): Why does the variable Name have a longer length than Policy or Total?
- Question (yzhu12-stat6250): What's the default length of the numeric variable Oyster?
- Answer (yzhu12-stat6250): 6



[Course Textbook Chapter 2, Problem 3]
* *Question (aalshehry−stat6250):* Where and how to use YEARCUTOFF option?
- Question (lzhao4−stat6250):  YEARCUTOFF= option has no effect in some cases?
- Answer (lzhao4−stat6250): The YEARCUTOFF= option has no effect when processing dates with four-digits years, processing dates already stored as SAS date values, and displaying dates with SAS date formats.
- Question (dlee117−stat6250): What date would 4/4/17 be interpreted as if YEARCUTOFF = 2017?
- Question (yzhu12-stat6250): How to define library?
- Answer (yzhu12-stat6250): You assign a library name (a libref) to it and specify a path, such as a directory path and use the libref as the first part of the file's two-level name (libref.filename) to reference the file within the library. You can use programming statements to assign library names. 



[Course Textbook Chapter 2, Problem 7]
* *Question (aalshehry−stat6250):* How to save your dataset in the permanent library?
- Question (lzhao4−stat6250): How to correctly assign a SAS libref?
- Question (dlee117−stat6250): What are the steps to reference a permanent SAS file?
- Question (yzhu12-stat6250): How can you modify system options?
- Answer (yzhu12-stat6250): I submit an OPTIONS statement and place an OPTIONS statement anywhere in a SAS program to change the current settings. Because the OPTIONS statement is global, the settings remain in effect until you modify them or until you end your SAS session. 



[Course Textbook Chapter 2, Problem 8]
* *Question (aalshehry−stat6250):* Without using the YEARCUTOFF= option, how would SAS interpret 11/11/20? Is it 1920 or 2020?
* *Answer (aalshehry−stat6250):* The default value of YEARCUTOFF= is 1920.
- Question (lzhao4−stat6250): How does YEARCUTOFF= option work on the interpretation of two-digits years?
- Question (dlee117−stat6250): Is the value for YEARCUTOFF the first year of the 100-year span or the last year?
- Question (yzhu12-stat6250): What step should we take before we access to SAS files that stored in a permanent SAS data library?
- Answer (yzhu12-stat6250): We must assign a libref.



[Course Textbook Chapter 2, Problem 9]
* *Question (aalshehry−stat6250):* If a SAS session is ended or a libref is deleted, does the library still exist?
* **Answer (aalshehry−stat6250): In these cases, SAS no longer has access to the files in the library.
- Question (lzhao4−stat6250): Libref exists only during the session in which it is created?
- Question (dlee117−stat6250): What is the default libref for temporary SAS files?
- Question (yzhu12-stat6250): What option do we add to suppress detailed information about the files?
- Answer (yzhu12-stat6250): NODS.



[basic_recipe_for_loading_data_from_remote_Excel_file (from Week 2 Overview)]
* *Question (aalshehry−stat6250):* Is it mandatory to use “filename tempfile clear;” step? Why?
- Question (lzhao−stat6250): Do we possible to transfer data from SAS dataset to an excel file? How? 
- Question (dlee117−stat6250): What does it mean to assign TEMP to the file name tempfile?
- Question (yzhu12-stat6250): Besides the method using "get" function to download URL, what other methods can be the substitute?



[optional: bonus_advanced_recipe_for_loading_data_from_remote_Excel_file (from Week 2 Overview)]
- Question (yzhu12-stat6250): What's the meaning of two command % and & in SAS?


