# **Database (SOC-3020), Fall 2026** 

# **Dr. Alessandro Agostini** 



# **Homework Assignment 3** 

Issued Tuesday 10 November 2026. Due as **zipped archive** uploaded into eCLASS by **Wednesday 18 November 2026 at noon** (12:00, system’s clock). Hardcopy: none (upon request only). 

# **Please note the following:** 

**1.** Deadline is *strict*. **Electronic deadline passed without submission implies mark 0 (zero)** . (Equivalently, you will not be admitted to enter the classroom for Quiz 3.) 

**2.** The number of students is: 1 to 3. See next. 

**2.1** Teams formed by **4 members or more are not permitted** (all students are not admitted to Quiz 3). **2.2** Although teams can be formed by students from any of the sections 003 to 004, it is preferable if students in a team belong to the same section. 

**3.** The homework must be written using L<sup>A</sup> TEX, either by installing one of your favourite versions<sup>1</sup> , or by using OVERLEAF, an easy-to-use online editor for L<sup>A</sup> TEX available at https://www.overleaf.com. **3.1** Any L<sup>A</sup> TEX template (OVERLEAF provides many) is okay. Teams are encouraged to create their own template, provided that the cover of their work contains the data required (see next). 

**3.2** The **cover** must contain the full name of the students in the team, their ID number and section. In particular, students shall be listed in increasing order by ID number; the name of the student who eventually uploads the homework to eCLASS shall be underlined. 

# **4. MODALITY OF SUBMISSION:** 

**+** One member of the team (say, the “team leader”) is required to upload into eCLASS one single **zipped archive** containing: 

(1) the L<sup>A</sup> TEX source file (extension .tex); 

(2) its compilation (.pdf file); 

(3) a folder with all images or figures (if any) used in L<sup>A</sup> TEX file (1), and all the screenshots reporting query results as produced by using your DBMS (see PARTICULAR SETTING); (4) a file 00X-ID-DDL.sql (see Exercise 1); 

(5) a file 00X-ID-DML.sql (see Exercise 1). 

**+** The **name of zipped archive** , as well the **name of each submitted file** (1) to (5) must be in format: 00X-ID (Example: 001-U2310123), where: 00X is the section of the team member who submits the homework to eCLASS and ID is his or her ID number. 

**5. PLAGIARISM WARNING!** Homework that containts elements of **plagiarism or cheating** , either among teams or from existing material (e.g., from the Internet, etc.) implies a mark 0/100 **for all teammates and all future homework assignments** . (Equivalently, **all team members will not be allowed to enter the next in-class quiz and successive** .) You may <u>not</u> copy source code (L<sup>A</sup> TEX, diagrams, etc.) or any other material from other people or the web. Moreover, dishonesty while discussing an academic integrity issue (i.e. lying to course staff) can result in a ‘F’ in the course. All violations of this collaboration policy will be referred to the appropriate University disciplinary board, with possible additional disciplinary action. Please ask the instructor (not TA!) if you are unsure. 

**5.1** Generative AI tools can be used **only if explicitly declared** and **only when explicitely allowed** . We will check your homework by plagiarism detection software that works both in standard form and over text produced by AI writing tools. 

> 1Among others are Texlive, Mactex, and Miktex. 

1 

**Database (SOC-3020), Fall 2026** _– Dr. Alessandro Agostini_ 

_Homework 3_ 2 

# **PARTICULAR SETTING:** 

You need the same technical setting you used in the Homework Assignment #2, that is, MYSQL SERVER and its standard graphical interface _phpMyAdmin_ (or any compatible console for MYSQL). 

**IMPORTANT:** You are allowed to use POSTGRESQL, provided that (1) the database you write (see Exercise 1) can be imported without any changes into MYSQL (ver. 8.0.18 or older), and (2) all queries you execute in POSTGRESQL can be executed in MYSQL without any — again: _any_ — changes. We shall possibly run your queries for verification and evaluation purposes. 

# **PROBLEMS AND EXERCISES:** 

**Exercise 1:** Consider following relational database (schema in diagrammatic notation and datatypes)<sup>2</sup> : 



<!-- Start of picture text -->
Customer Actor<br>cust_id CHAR(8) actno INT<br>fname VARCHAR(50) fname VARCHAR(50)<br>sname VARCHAR(50) sname VARCHAR(50)<br>dob DATE dob DATE<br>Rental fee INT dod DATE<br>renno INT picture BLOB<br>due DATE makes<br>cust_id CHAR(8)<br>performs<br>includes<br>Movie Acts<br>Rental_copy movno INT contains actno INT<br>renno INT mname VARCHAR(50) movno INT<br>copyno INT genre VARCHAR(50) rolno INT<br>status CHAR(1) language VARCHAR(20) description TEXT<br>publisher VARCHAR(30)<br>writes year INT typical_of<br>is_included age_limit INT<br>rating NUMBER(3,1)<br>Copy Role<br>of rolno INT<br>copyno INT<br>format VARCHAR(6) fname VARCHAR(50)<br>statusmovno CHAR(1)INT located_in snamealias VARCHAR(50)VARCHAR(50)<br>stono INT description TEXT<br>written_for<br>Store<br>Review stono INT has_worker Employee<br>cust_id CHAR(8) street VARCHAR(50) empno INT<br>movno INT zip CHAR(6) fname VARCHAR(50)<br>points INT city VARCHAR(20) managed_by sname VARCHAR(50)<br>review_text TEXT phone VARCHAR(20) active_bool BOOLEAN<br>stono INT<br>empno INT<br><!-- End of picture text -->

Figure 1: A database for a movie rental business domain. 

**NOTE ON NOTATION:** Each tagged arrow represents a foreign key (red) constraint between two joinable relations and its intended interpretation (reading convention: left-to-right or top-tobottom). As usual, the underlined attributes of a relation form the primary key for that relation. 

2Attributes dob and dod mean “date of birth” and “date of death”, respectively. 

**Database (SOC-3020), Fall 2026** _– Dr. Alessandro Agostini_ 

_Homework 3_ 3 

1. By using SQL-DDL clauses provided by the DBMS you use, write in a file the CREATE TABLE statement for each relation and import the file into the system. This is the file 00X-ID-DDL.sql referred as file (4) in the MODALITY OF SUBMISSION (page 1). 

Write each statement also directly into your document. 

2. By using SQL-DML clauses provided by the DBMS you use, write in a file the INSERT INTO statements to populate each relation with proper data according to given datatypes. This is the file 00X-ID-DML.sql referred as file (5) in the MODALITY OF SUBMISSION (page 1). Write each statement also directly into your document. 

REMARK: If your DBMS does not provide exactly the same datatypes among those mentioned in the schema above, use the available datatype closer in meaning. 

**IMPORTANT:** The average number of rows with full data inserted to each relation is expected and required to be not less than 20. **You can use generative AI to generate sample data** as required by the INSERT INTO...VALUES statements. 

**IMPORTANT:** The files 00X-ID-DDL.sql and 00X-ID-DML.sql shall be neat and **contain code commented by you – not by AI!** Moreover, the files shall **not contain autogenerated system code – generated by** MYSQL **!** In other words, these two files shall contain ONLY SQL standard code from MYSQL: the SQL tables (DDL data) and data instances (DML data). You need to “polish” them and clean out all code not striclty related to the logical schema produced in Exercise 2 and completed with constraints and possibly triggers. 

**Exercise 2:** Consider the following list of fifteen English queries on the database in Figure 2. 

1. List all information regarding stores in Trento and Tashkent. 

2. List the names, age limits and years of movies that are in English but are not published by Goldeneye BC. Sort the results according to the name of the movie in ascending order. 

3. List the names, dates of birth and death of actors whose surname starts with an F or an S, and whose date of birth is unknown, or who have a date of death. 

4. List the city and phone number of the store in which Ivan Ivanovich works. 

5. List the names of actors whose date of death is known and who have acted in at least one movie released after 2020. Sort the results according to surname in descending order. 

6. List the names of actors who have acted a role as himself or herself. Sort the results according to surname, and then according to first name, both in ascending order. 

7. List the movie numbers, names and years of movies that have been released in the second decade of the 2000s, but of which there exists no copy in BluRay format. 

8. List the names and dates of birth of customers who have never rented a movie but who have given at least one review. 

9. List the number of movies released between the years 2000-2026. Rename the column in the result table descriptively. 

**Database (SOC-3020), Fall 2026** _– Dr. Alessandro Agostini_ 

_Homework 3_ 4 

10. List the names of actors who have acted in the movie _Miracle_ by Gavin O’Connor (2004) and list the names of the roles they have played in that movie. Rename the columns in the result table descriptively. 

11. List the name, year and genre of the oldest movie published by Goldeneye BC. 

12. List the actor numbers and full names of actors who have acted in at least five different movies. 

13. List the names of customers who have rented exactly the same movie copy that Anna Karenina (customer id ’karenina’) has rented, whenever. 

14. List the numbers of movie copies located in stores by city and status of the copy. Sort the results by city in ascending order. 

15. List the numbers of movie copies by movie number and movie name. Disregard movies of which there are less than six copies, regardless of the status of the copy. Sort the results according to the number of the copies in descending order. 

Then, for each query _Q_ in the list, do the following (see also REMARK 1 in light orange box below): 

- (a) Rewrite _Q_ by using plain SQL. Use the simplest form with the most common clauses you know. 

**TECHNICAL NOTE 1:** For _plain_ SQL we mean you need to write the code directly in the document, possibly by using the standard L<sup>A</sup> TEX environment provided by package _listings_ . Example: 

\begin{lstlisting}[language=SQL] SELECT name FROM Student AS S 

WHERE S.dept_name = ’CSE’; \end{lstlisting} 

**IMPORTANT:** For this task, you are **not allowed to use generative AI.** We will assign 0 to your homework, if we discover that you used it. If you do not know how to translate a given English query to SQL standard, no problem: skip it and go to task (b) below. In this case, you are required to write the following sentence or equivalent in the exact place you would write the SQL query otherwise: 

“I [We] don’t know how to solve this query.” 

**In lack of a correct SQL query or the sentence above, we penalize your work by -1 points in Quiz 3 for each missed sentence** . 

- (b) Rewrite _Q_ by using your **most preferred generative AI tool** *. Write the query in your document by using plain SQL (see previous Technical Note 1). 

   - **IMPORTANT:** You are asked to: (1) make explicit the name and version of the AI 

   - tool/software/model you used to generate the query. If you use the same tool for all queries, it is enough that you declare the name and version of the tool only when you write the first query in the list; (2) write the day when you accessed the tool —write “Accessed: 2026-11-dd”, where “dd” is the day; and (3) make explicit the _PROMPT_ (one step or many) you input to the AI tool to obtain the query. 

**Database (SOC-3020), Fall 2026** _– Dr. Alessandro Agostini_ 

_Homework 3_ 5 

- (c) Execute **one** of the two SQL queries you wrote for task (a) (if you produced it) and (b) — _you_ choose what query — on the database in Exercise 1, and **screen-shot the query and its result** . 

**TECHNICAL NOTE 2:** The screenshot is expected to contain **both the query and the result** . If the query’s result contains more rows than those a screen-shot can contain and still be OK, then limit the screen-shot by including less rows, and write how many rows you did not showed in the result for displaying purposes. 

- (d) Embed the screen-shot in your document. Two cases arise: Case 1. The query executed correctly. Then consider the next English query in the list. Case 2. The execution of the query produced a “syntax error” or any other execution error. Then: 

   - debug your query (refer to your DBMS’s manual, if necessary) and execute it again (and again, if necessary) until you managed to solve the error and correctly execute the query; 

   - screen-shot **both the query you have eventually, correctly executed and its result** . Embed it into your document; 

   - explain in short what kind of issue you had to correctly execute the query. Be brief yet precise to identify the issue(s) you faced. 

If, after several debugging cycles, you are still unable to execute the query correctly, explain the reasons. Then move forward and consider the next English query in the list. 

**REMARK 1:** The tasks (a) to (d) above have to be presented in sequence **for each English query** _Q_ **in the list** . For example, for any query _n_ , you will have a structure of your answer like this (you might like to show such structure in the table of contents): 

   1. English query (the query _n_ from the list); 

   2. query in plain SQL by you (task (a)) or the sentence “I [We] don’t know how to solve this query.” Write the code within a “lstlisting” environment (see Technical Note 1 above); 

   3. query by AI-generative tool (task (b)). In this case, specifically write: 

      - + name of tool used, 

      - + version or tool used (if available) and weblink, 

      - + exact _prompt_ used to obtain the desired result, 

      - + the resulting SQL query generated (no editing by yourself here!); 

   4. one of the queries from tasks (a) (if any) and (b), re-written by using the SQL interface _phpMyAdmin_ (or equivalent), as well as the result after execution, as explained in tasks (c) and (d) above. 

- **Exercise 3:** Read window functions concepts and syntax defined in MYSQL, available online here: 

https://dev.mysql.com/doc/refman/8.4/en/window-functions-usage.html. 

Now consider the window functions provided by MYSQL (version 8) and listed here: 

https://dev.mysql.com/doc/refman/8.4/en/window-function-descriptions.html 

**Database (SOC-3020), Fall 2026** _– Dr. Alessandro Agostini_ 

_Homework 3_ 6 

or, more explicitely, these functions: 

CUME_DIST ( ) DENSE_RANK( ) FIRST_VALUE ( ) LAG( ) LAST_VALUE( ) LEAD( ) NTH_VALUE( ) NTILE ( ) PERCENT_RANK( ) RANK( ) ROW_NUMBER( ) 

Then, **for minimum three to maximum five functions** listed above, for each function _F_ you choose, do the following: 

- (a) Specify the function _F_ — simply write the function as it is written in the list above. 

- (b) Provide an English query, say _Q_ , that uses _F_ and the database schema in Figure 2 as you implemented in Exercise 1. 

- (c) Rewrite _Q_ by using plain SQL. See previous Technical Note 1. 

**IMPORTANT:** For this task, you might want to use your **most preferred generative AI tool** (but it could be possible you don’t). In any case, _after_ the SQL query you propose as a solution equivalent to _Q_ , write the following information: 

1. AI generative tool used: Yes / No ( _specify your case_ ). If you write “Yes”, then write: (*) 

   2. name of tool used (if used), version and weblink; 

   3. exact _prompt_ used to obtain the desired result; 

   4. information on your editing of AI generated result in 3, if any editing is done. Write “no editing”, otherwise. 

- (d) Execute the SQL query as produced in (c) on the database you created in Exercise 1, and screenshot the query and its result (see Technical Note 2). 

- (e) Embed the screen-shot in your document. Two cases arise: Case 1. The query executed correctly. Then consider the next window function that you have chosen. 

Case 2. The execution of the query produced a “syntax error” or any other execution error. Then: 

- debug your query (refer to your DBMS’s manual, if necessary) and execute it again (and again, if necessary) until you managed to solve the error and correctly execute the query; 

- screen-shot **both the query you have eventually, correctly executed and its result** . Embed it into your document; 

- explain in short what kind of issue you had to correctly execute the query. Be brief yet precise to identify the issue(s) you faced. 

If, after several debugging cycles, you are still unable to execute the query correctly, explain the reasons. Then move forward and consider the next chosen window function. 

**Database (SOC-3020), Fall 2026** _– Dr. Alessandro Agostini_ 

_Homework 3_ 7 

**REMARK 2:** The tasks (a) to (e) above have to be presented in sequence **for each window function** _F_ **you have chosen** . 

# **Exercise 4:** Read this technical note: 

**TECHNICAL NOTE: (1)** In this exercise, where you need to translate a SQL query into RA (Relational Algebra) or ERA (Extended or Generalized RA), use symbols and statements as defined in this box. If the SQL query contains clauses IN or NOT IN applied to a subquery _S_ — namely: “...IN S” or “...NOT IN S” —, use symbols _∈, /∈_ , respectively — so: _... ∈ S_ or _... ∈/ S_ , in your translation, where _S_ shall be the variable assigned to the subquery via the assignment operator “ _←_ ”. If the SQL query contains clauses EXISTS or NOT EXISTS before a certain subquery, say _Q_ , then write “ _∃x Q_ ( _x_ )”, “ _¬∃x Q_ ( _x_ )”, respectively, in your translation, where _Q_ shall be the variable assigned to the subquery via the assignment operator “ _←_ ”. If the SQL query contains clauses ALL or SOME, with any arithmetic symbol for comparison <, <=, =, <>, >=, > on the left, before a certain subquery, say _S_ , then translate it by writing, for example, “ _∀x ∈ S_ ( _A < s_ )”, if <ALL is used to compare attribute _A_ ’s value with all members of _S_ . (Similarly, write “ _∃x ∈ S_ ( _A < s_ )”, if <SOME is used.) If the SQL query contains a Boolean operator AND,OR, NOT, then use _∧_ , _∨_ , _¬_ , respectively, in your translation. If the SQL query contains clause IS NULL or IS NOT NULL, then write = NULL or _̸_ = NULL, respectively, in your translation. **(2)** For the sake of translation from SQL into RA or ERA, remember that SELECT and SELECT DISTINCT are equivalent. **(3)** We assume that SQL’s aggregate function COUNT(DISTINCT ...) translates into RA’s function **countdistinct** (...), and COUNT(...) translates into RA’s function **count** (...). All other “classical” SQL’s aggregate functions (e.g., _min_ (), _max_ (), _avg_ (),...) translate to ERA as they are denoted in SQL. For the operations, use the symbols we used: _σ_ , Π, _×_ , _∪_ , _∩_ , _−_ , _ρ_ , _1_ , _~~1~~_ , _~~1~~_ ~~,~~ _~~1~~_ ~~,~~ _G_ . 

Consider following relational database (schema in diagrammatic notation and datatypes): 



<!-- Start of picture text -->
Post User Relationships<br>postno INT posts userno INT has userno1 INT<br>description TEXT username VARCHAR(50) userno2 INT<br>content BLOB featured post email VARCHAR(50) has type VARCHAR(10)<br>reputation INT country CHAR(2)<br>userno INT postno INT<br>concerns<br>Reaction Message<br>userno INT reacts sends userno_sender INT<br>postno INT userno_recipient INT<br>reaction_type VARCHAR(12) sent_at DATETIME<br>receives received_at DATETIME<br>content VARCHAR(255)<br>read BOOLEAN<br><!-- End of picture text -->

Figure 2: A database for a small social media. 

Consider the following list of fifteen English queries on the database in Figure 2. 

1. Retrieve data for the information of users from Uzbekistan (UZ) and Italy (IT). 

2. List the user numbers, user names, countries and emails of users who are Uzbek (UZ) but have no featured post. Sort the results according to user name in ascending order. 

**Database (SOC-3020), Fall 2026** _– Dr. Alessandro Agostini_ 

_Homework 3_ 8 

3. List post numbers, descriptions and user numbers who made the post, of posts which description starts with an S or an R, and that have been posted by users whose user number is 1001 or 1003. 

4. List user names and emails of users who have a featured post with no description. 

5. List the post numbers and descriptions of posts which at least one Uzbek (UZ) user has considered funny. Sort the results according to post number in descending order. 

6. List the contents and user numbers of the receivers of messages which were sent by an user with user number 1001 or 1003, and who has reacted to some post at least once. Sort the results according to the user number, and then according to content, both in ascending order. 

7. List the post numbers, contents and reputations of posts which have a reputation greater than 0, but which no one has ever considered funny. 

8. List the user names, emails and countries of users who have never posted anything but who have at least once reacted to a post. 

9. List the average of post reputations with a reputation greater than 0. Rename the column in the result table descriptively. 

10. List the user names, emails, countries, and reaction types and post numbers which the reactions concern, but only from users who are married. Rename the columns in the result table descriptively. 

11. List the contents, sender user number, and the time the message was sent of the oldest unread message. 

12. List the user names and emails of users who have sent messages to exactly six different users. 

13. List the user names and countries of users who have posted a post which has received the at least one similar type of reaction as any post made by user 1004. 

14. List the numbers of users by country and relationship type. Sort the results by country in ascending order. 

15. List the numbers of sent messages by the sender’s country and message read status. Disregard senders with less than four sent messages, regardless of the message read status. Sort the results according to the number of messages sent in descending order. 

Then, for each query _Q_ in the list, do: 

- (a) Rewrite _Q_ by using SQL standard and, soon after, by using the language of relational algebra. Ignore ORDER BY if _Q_ uses it. Refer to Technical Note above for the logical language to use. 

**IMPORTANT:** For this task, use your preferred AI tool. See next remark. 

**Database (SOC-3020), Fall 2026** _– Dr. Alessandro Agostini_ 

_Homework 3_ 9 

**REMARK:** The task (a) shall be presented **in sequence for each English query** _Q_ **in the list** . For example, for any query _n_ , you will have a structure of your answer like this (you might like to show such structure in the table of contents): 

1. English query (the query _n_ from the list); 

2. query in plain SQL; 

3. expression in RA or ERA by AI-generative tool. Write: 

   - + name of tool used, 

   - + version of tool used (if available) and weblink, 

   - + exact _prompt_ used to obtain the desired result. 

**FINAL REMARK:** Be ready to complete any task described above in the in-class Quiz 3. 

End of Homework Assignment 3 

