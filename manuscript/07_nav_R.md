# Managing files in R

In this lesson, we will continue our tour of ways in which you will be managing files as a data scientist. In the previous lesson, you learned about the Terminal and its command-based interface to the file system on RStudio Cloud. In this lesson, you will learn in small part about the R programming language and in large part about specfic tools within R to manage files. You will learn much more about R for its capabilities in data science work in future courses.

### What is R?

Simply put, R is a programming language. That is, R provides a syntax and a suite of functions to automate a variety of tasks that you'll be faced with as a data scientist. R has tools to automate view, summarize, and manage data. These topics will all be covered in later courses. R also has tools for file management. The focus of this lesson is on a small set of functions that you may find useful in managing your files.

### Why manage files in R?

As a data scientist, you will find it very useful to automate the management and organization of files. In the previous lesson, you learned about the power of the Terminal to run commands that allow you to more efficiently manage files than standard clicking and typing. However, for some tasks with larger scale data projects, it will be easier to work with files programatically in R rather than at the Terminal. Why? Because R is programming language, you will be able to manage files in complex situations where your actions are dependent on lot of other information. For example, if you are working with hundreds of different files, moving them to a location that depends on information in the files is much easier with a programming language such as R rather than at the Terminal. Also, in order to completely document your work in going from raw files to finished products, a good approach is to combine your data work in R (to be covered in later courses) with your file organization work in R.

### Navigating to R in RStudio Cloud

When you open a project in RStudio Cloud, you will see a Console pane that is immediately next to the Terminal pane. Usually this pane is automatically open when you open a project. The `>` that you see in the R console is called the **R prompt**. It is analogous to the Terminal prompt in that it is where you can type and enter R commands.

![Locating the Console in RStudio Cloud](images/07_nav_R/07_fileorganization_nav_R-3.png)

### File system setup

We're going to be using the same file system setup as in the previous lesson. The file system is shown below. Only the `raw_data` and `raw_code` folders contain files. In this lesson, we will be working within this file system to illustrate useful file manipulation functions within R.

![Example file system](images/07_nav_R/07_fileorganization_nav_R-4.png)

### Important functions

#### What is my working directory?

Recall from the previous lesson that a **working directory** is the folder that you are currently in within a file system. We discussed that the working directory within the Terminal may be different from the working directory within R, and both of these may be different from the Files pane in RStudio. To determine your working directory in R, you can use the `getwd()` function, which stands for "get working directory." When you type `getwd()` at the R prompt and hit enter, you will see the absolute path to your working directory displayed in quotes on a new line. As with working in the Terminal, knowing the working directory in R is important because when you run code that refers to other files, R will search for those files relative to this directory. `getwd()` is analogous to `pwd` in the Terminal.

![getwd()](images/07_nav_R/07_fileorganization_nav_R-6.png)

#### Set the working directory

In Terminal you learned about the `cd` command to change the current (working) directory. In R, use the `setwd()` function, which stands for "set working directory." Inside the parentheses, type an absolute or relative path in quotes. Just as in the Terminal, tab completion can save typing time and help prevent incorrect spelling. When you hit tab after typing part of a path, RStudio provide a drop down menu of files and folders that fit what you have typed. You can select between them with the arrow keys or your mouse and hit enter to autocomplete. Note also that the absolute path to the current working directory is displayed in the status bar beneath the Console tab. The working directory is not automatically updated or reflected in the Files pane however.

![setwd()](images/07_nav_R/07_fileorganization_nav_R-7.png)

#### What is in this folder?

In Terminal you learned about the `ls` command for listing the contents of a directory. In R, use the `list.files()` function. Without anything in the parentheses, R will list the files in the current working directory. Otherwise, you can include a relative or absolute path in quotes. In the example we see that using no path gives the same result as specifying the current directory with a period. When we list the files in the `raw_code` directory, four files are listed. The numbers in the square brackets just help us count in the displayed output. An option when using `list.files()` is to type `full.names = TRUE` after the initial path and a comma. Doing this displays the full relative paths to those files. Note that if the path ends in a forward slash, there will be two forward slashes before the filename in the output. This is not a problem, but if you prefer to not have two forward slashes, omit the trailing forward slash when you type the path.

![list.files()](images/07_nav_R/07_fileorganization_nav_R-8.png)

#### Create a file

In Terminal you learned about the `touch` command to create a blank file. In R, use the `file.create()` function. In parentheses, provide a path to the file to create. If this is successful, R will display `TRUE` and `FALSE` otherwise. You can verify that the file has been created by using `list.files()`. As in Terminal, you can quickly cycle through recent commands using the up and down arrow keys.

![file.create()](images/07_nav_R/07_fileorganization_nav_R-9.png)

#### Moving and renaming a file

In Terminal you learned about the `mv` command for moving and renaming files. In R, use the `file.rename()` function. In the parentheses, you provide two paths separated by a comma. The first path is the path to the origin file. The second path is the path to the destination file. In the first example, we move the `data3.txt` file and keep the same name by specifying a different sequence of folders at the beginning of the second path and keeping the same file name. In the second example, we move and rename simultaneously by specifying a different sequence of folders and a different file name. If the renaming is successful, R will display `TRUE` and `FALSE` otherwise.

![file.rename()](images/07_nav_R/07_fileorganization_nav_R-10.png)

#### Copy a file

In Terminal you learned about the `cp` command for copying and renaming files. In R, use the `file.copy()` function. This function works similarly to `file.rename()` in that you have to supply the path to the original file first and the path to the destination second. If the copy is successful, R will display `TRUE` and `FALSE` otherwise. The first example copies the `data3_renamed.txt` file to the `data3.txt` file. In the second example, we try to do this again but fail because `data3.txt` already exists, and R will not overwrite a file by default. In example 3, we specify `overwrite = TRUE` after the two paths and a comma to explicitly overwrite the `data3.txt` file.

![file.copy()](images/07_nav_R/07_fileorganization_nav_R-11.png)

#### Remove a file

In Terminal you learned about the `rm` command for deleting files. In R, use the `file.remove()` function. In the parentheses, provide a path to the file you want to delete in quotes. If the deletion is successful, R will display `TRUE` and `FALSE` otherwise.

![file.remove()](images/07_nav_R/07_fileorganization_nav_R-12.png)

#### Does a file exist?

In Terminal you used the `ls` command to list the contents of a directory for verifying what files and folders are present. If you want to check whether a particular file exists, you can use the `file.exists()` function in R. In the parentheses, provide a path to the file of interest. In the first example, we show the usage for a single file. For `data1.txt`, R displays `TRUE` because this file exists. In the second example, we show the usage if you want to check the existence of multiple files. The multiple files are specified in what is called a **character vector**. The two paths are separated by a comma in the `c()` function which is the concantenation function. In this case, R displays `TRUE` then `FALSE` because `data2.txt` exists but `data4.txt` does not. You will learn much more about character vectors and the `c()` function in later courses devoted to R. Note that the other functions we covered in this lesson (except `getwd()` and `setwd()`) can also be used on multiple files by supplying **character vectors** of paths instead of single paths. You will have a chance to try these out when you learn more about R and begin working on projects.

![file.exists()](images/07_nav_R/07_fileorganization_nav_R-13.png)

### Summary

In this lesson, you learned about R functions that are analogous to Terminal commands for managing files. As you work on projects, you'll gain an appreciation for the benefits of managing files using a programming language.

### Slides and Video

![Managing files in R](https://www.youtube.com/watch?v=maSo_Byarvw)

* [Slides](https://docs.google.com/presentation/d/1T_KaKPNffgoHSOqM65c_E5AI93KK2BYRBhJNXjOxRmc/edit?usp=sharing)


{quiz, id: quiz_07_nav_R}

### Managing files in R quiz

{choose-answers: 3}
? Which of the following functions displays `TRUE` or `FALSE` after completion?

C) `file.create()`
C) `file.rename()`
C) `file.copy()`
C) `file.remove()`
C) `file.exists()`
o) `getwd()`
o) `setwd()`
o) `list.files()`

{choose-answers: 4}
? Which of the following R function and Terminal command pairs perform the same function?

C) `getwd()` and `pwd`
C) `setwd()` and `cd`
C) `list.files()` and `ls`
C) `file.create()` and `touch`
C) `file.rename()` and `mv`
C) `file.copy()` and `cp`
C) `file.remove()` and `rm`
o) `getwd()` and `cd`
o) `setwd()` and `pwd`
o) `file.rename()` and `rnm`
o) `file.rename()` and `cp`
o) `file.copy()` and `mv`
o) `file.remove()` and `del`

{choose-answers: 4}
? Refer to the file system diagram below. The current working directory is `code`. Which of the following Terminal commands and/or R functions will move the `tidy_data1.R` file in the `raw_code` directory to the `final_code` directory?

![Example file system](images/07_nav_R/07_fileorganization_nav_R-4.png)

C) `mv raw_code/tidy_data1.R final_code/`
C) `mv ../code/raw_code/tidy_data1.R ../code/final_code/`
C) `file.rename("raw_code/tidy_data1.R", "final_code/tidy_data1.R")`
C) `file.rename("../code/raw_code/tidy_data1.R", "../code/final_code/tidy_data1.R")`
o) `cp raw_code/tidy_data1.R final_code/`
o) `cp tidy_data1.R ../final_code/`
o) `mv tidy_data1.R ../final_code/`
o) `cp ../code/raw_code/tidy_data1.R ../code/final_code/`
o) `file.copy("raw_code/tidy_data1.R", "final_code/tidy_data1.R")`
o) `file.rename("tidy_data1.R", "../final_code/tidy_data1.R")`
o) `file.copy("../code/raw_code/tidy_data1.R", "../code/final_code/tidy_data1.R")`

{/quiz}
