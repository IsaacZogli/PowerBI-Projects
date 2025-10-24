Data Source.
The Student Performance Dataset is a local dataset which presents academic performance data using variables like Student_Id, Name, Gender, Age, Class, Math_Score, Science_Score , English_Score and Remarks.


Data Cleaning Steps Taken To Clean The Dataset.
1.	The  Student Performance dataset  was loaded unto the PowerBI Desktop using the  “get data” option. 
2.	The data was then transferred to Power Query using the “ Transform Data” option.
3.	Afterwards, a series of data cleaning steps were taken on the dataset under each variable:
4.	Name:
•	The name column was split into two columns; “First Name” and  “Surname” using a delimiter and  the delimiter was the “SPACE” in between the two names under the Name column.
5.	Gender:
•	Using our new  First Name column , we found out that a woman’s name was assigned to a Gender, “Male” or a man’s name was assigned to a Gender, ‘Female’ using logic.
•	Therefore, we checked for unique names under the new First Name column and found out that there five unique names used under the First Name column. That is, Abena, Ama, Esi, Kojo and Yaw.
•	Through this information, we created a new  Gender column using the “Conditional Column” option under the Add Column. That is, Abena = Female, Ama = Female, Esi = Female , Kojo = Male and Yaw = Male.
•	The old Gender column was then deleted.
6.	Age:
•	From the Age column we noticed that the column was in  a ‘Text’ format instead of ‘Numeric’ since age ‘sixteen’ was typed in words.
•	From this information, we replaced ‘sixteen’ with an original numeric value 16 using the ‘Replace Value’ option.
•	Then, changed the type of data from a ‘Text’ to a ‘Whole Number’ using the ‘Change Type’ option.
•	Also, we handled the missing values by replacing ‘null’ entries with the ‘average age’ since there were no outliers.
7.	Class:
•	From the class column, we realised the classes were not in a standardized  format since they were acronyms(i.e. JHS and SHS).
•	Therefore, we standardized them into an UPPERCASE format using the Transform option.
•	Also, from observation, we realised that there was space in between the “JHS 2” under the Class column.
•	Using Replace Value option, we replaced it with ‘JHS2’.
8.	Math_Score:
•	From the Math_Score column we noticed that the column was in  a ‘Text’ format instead of ‘Numeric’ since  score 80 and missing values were typed in words(eighty and N/A respectively).
•	From this information, we replaced ‘eighty’ with an original numeric value 80 using the ‘Replace Value’ option.
•	Also, replaced ‘N/A’ with  “        “ (nothing).
•	Then, changed the type of data from a ‘Text’ to a ‘Whole Number’ using the ‘Change Type’ option.
•	Also, we handled the missing values by replacing ‘null’ entries with the ‘average math score’ since there were no outliers.
9.	Science_Score:
•	From the Science_Score column we noticed that the column was in  a ‘Text’ format instead of ‘Numeric’ since  missing values(N/A)  was typed in words.
•	From this, we replaced ‘N/A’ with  “        “ (nothing) from the Replaced Value option.
•	Then, changed the type of data from a ‘Text’ to a ‘Whole Number’ using the ‘Change Type’ option.
•	Afterwards, we handled the missing values by replacing ‘null’ entries with the ‘average science score’ since there were no outliers.
10.	English_Score:
•	From the English_Score column we noticed that the column was in  a ‘Text’ format instead of ‘Numeric’ since  score 90 was typed in words ‘ninety’.
•	From this information, we replaced ‘ninety’ with an original numeric value 90 using the ‘Replace Value’ option.
•	Then, changed the type of data from a ‘Text’ to a ‘Whole Number’ using the ‘Change Type’ option.
•	Also, we handled the missing values by replacing ‘null’ entries with the ‘average english score’ since there were no outliers.
11.	Remarks:
•	From observation, we realised that under the Remarks column there were inconsistency. Example, ‘Kojo Yankson in SHS1 got 66 in Maths, 1 in Science and 9 in English was given an ‘Excellent’ Remark.
•	Therefore, we created an Average_Score column that calculated the average score of each student from the three subject scores(i.e. Math_Score, Science_Score and English_Score)
•	Then using conditional column, we created a new column called Teachers Remarks where; 
o	If a student got an Average_Score less than or equal to 40, he or she was assigned with a Teachers Remark of  ‘Needs Improvement.’
o	If a student got an Average_Score less than or equal to 60, he or she was assigned with a Teachers Remark of  ‘Average.’
o	If a student got an Average_Score less than 80, he or she was assigned with a Teachers Remark of  ‘Good.’
o	And finally, if a student got an Average_Score greater than or equal to 80, he or she was assigned with a Teachers Remark of  ‘Excellent.’
•	The Remark column was then deleted.


Challenges Faced In Cleaning The Dataset.
1.	Inconsistent Data Types.
2.	Missing or Null Values.
3.	Inconsistent Text Formatting.
4.	Logical issues.


