# File Naming

This is going to seem like a silly topic to have a whole lecture on. But one of the most frustrating things when looking at someone's data science project is to see a set of files that are completely scattered with names that don't make any sense. It also makes it harder to search for files if they don't have a consistent naming scheme. 

One of the best organized file naming systems is due to [Jenny Bryan](http://www2.stat.duke.edu/~rcs46/lectures_2015/01-markdown-git/slides/naming-slides/naming-slides.pdf) who gives three key principles of file naming for data science projects. Files should be

* Machine readable
* Human readable
* Be nicely ordered

If your files have these three characteristics, then it will be easy for you to search for them (machine readable), easy for you to understand what is in the files (human readable), and easy for you to glance at a whole folder and understand the organization (be nicely ordered). We'll now discuss some concrete rules that will help you achieve these goals. 


### Machine readable files

The machine we are talking about when we say "machine readable" is a computer. To make a file machine readable means to make it easy for you to use the machine to search for it. Let's see which one of the following examples are good example of machine readable files and which are not. 

- Avoid spaces: *2013 my report.md* is a not good name but *2013_my_report.md* is.
- Avoid punctuation: *malik's_report.md* is not a good name but *maliks_report.md* is.
- Avoid accented characters: *01_zoë_report.md* is not a good name but *01_zoe_report.md* is.
- Avoid case sensitivity: *AdamHooverReport.md* is not a good name but *adam-hoover-report.md* is.
- Use delimeters: *executivereportpepsiv1.md* is not a good name but *executive_report_pepsi_v1.md* is.

So to wrap up, spaces, punctuations, and periods should be avoided but underscores and dashes are recommended. You should always use lowercase since you don't have to later remember if the name of the file contained lowercase or uppercase letters. Another suggestion is the use of delimiters (hyphens or underscores) instead of combining all the words together. The use of delimiters makes it easier to look for files on your computer or in R and to extract information from the file names like the image below.

![Extracting information from properly named files](images/03_file_naming/03_fileorganization_file_naming-3.png)

### Human readable files

What does it mean for a file to be human readable? A file name is human readable if the name tells you something informative about the content of the file. For instance, the name `analysis.R` does not tell you what is in the file especially if you do multiple analyses at the same time. Is this analysis about the project you did for your client X or your client Y? Is it preliminary analysis or your final analysis? A better name maybe would be `2017-exploratory_analysis_crime.R`. The ordering of the information is mostly up to you but make sure the ordering makes sense. For better browsing of your files, it is better to use the dates and numbers in the beginning of the file name.


### Be nicely ordered

By using dates, you can sort your files based on chronological order. Dates are preferred to be in the ISO8601 format. In the United States we mainly use the mm-dd-yyyy format. If we use this format for naming files, files will be first sorted based on month, then day, then year. However for browsing purposes it is better to sort files based on year, then month, and then day and, therefore, the yyyy-mm-dd format, also known as the ISO8601 format, is better. Therefore, `2017-05-21-analysis-cust001.R` is preferred to `05-21-2017-analysis-cust001.R`.

If dates are not relevant for your file naming, put something numeric first. For instance if you're dealing with multiple reports, you can add a reportxxx to the beginning of the file name so you can easily sort files by the report number.

![Using numbers for ordering files](images/03_file_naming/03_fileorganization_file_naming-6.png)

In addition to making sure your files can be nicely ordered, always left-pad numbers bu zeros. That is first set a max number of digits for your numbers determined by how many files you will potentially have. So if you may not have more than 1000 files you can choose three digits. If not more than a hundred you can choose two digits and so on. Once you know the number of digits, left-pad numbers with zeros to satisfy the number of digits you determined in the first step. In other words, if you're using three digits, instead of writing 1 write 001 and instead of writing 17 write 017.


![Left padding numbers with zeros](images/03_file_naming/03_fileorganization_file_naming-7.png)

  
### Slides and Video

![File Naming](https://www.youtube.com/watch?v=H2AZ27LgW_U)

* [Slides](https://docs.google.com/presentation/d/1vQEUA7UqgEWrCUZv25t6qpwbLwrZo9oC0y0zUjLRUT4/edit?usp=sharing)

{quiz, id: quiz_03_file_naming}

### File Naming quiz

{choose-answers:4}
? What are the three elements of best file naming practices?

C) Human readability, machine readability, and proper ordering
C) Proper ordering, human readability, and machine readability
C) Machine readability, [roper ordering, and human readability
o) Abbreviation, having numbers at the end of the name, and proper ordering
o) Human readability, machine readability, and only using letters and spaces
o) Abbreviation, machine readability, and proper ordering
o) Having numbers at the end of the name, human readability,and proper ordering

{choose-answers:4}
? Which one is *not* considered good practice in file naming?

C) Always use commas
C) Always use the longest possible name
C) Ensure that it cannot be understood by humans
o) Use delimiters such as underscores
o) Do not use accented letters
o) Avoid spaces
o) Avoid case sensitivity
o) Avoid punctuation 

{choose-answers:4}
? Which one of the following file names does NOT follow best file naming practices?

C) 06-23-2015_baltimore_school_001.txt
C) 09-29-2015_baltimore_school_007.txt
o) 2015-06-23_baltimore_school_001.txt
o) 2015-09-29_baltimore_school_020.txt
o) 2015_baltimore_school_001.txt
o) 2015_baltimore_school_001.txt
o) 2015-06_baltimore_school_001.txt
o) 2015-09_baltimore_school_001.txt

{choose-answers:4}
? Which one of the following file names follows best file naming practices?

C) helper01_analysis_gender.R
C) helper02_analysis_gender.R
o) Helper1AnalysisGender.R
o) helper 1 analysis gender.R
o) helper 3 analysis g.R
o) helper_analysis_gender_01.R
o) helper01_analysis_gender$.R
o) helper01,analysis_gender.R

{choose-answers:4}
? Which one of the following file names follows best file naming practices?

C) fig_007_analysis_subway_delays.png
o) fig 7.png
o) finalfigure.png
o) fig_analysis_subway_delays_007.png
o) FIG_007_Analysis_Subway_Delays.png
o) Delays,Figures.png
o) analysis subway delays.png


{/quiz}

