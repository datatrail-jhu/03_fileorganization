# Managing files in R

In this lesson, we will continue our tour of ways in which you will be managing files as a data scientist. In the previous lesson, you learned about the Terminal and its command-based interface to the file system on RStudio Cloud. In this lesson, you will learn in small part about the R programming language and in large part about specfic tools within R to manage files. You will learn much more about R for its capabilities in data science work in future courses.

### What is R?

Simply put, R is a programming language. That is, R provides a syntax and a suite of functions to automate a variety of tasks that you'll be faced with as a data scientist. R has tools to automate view, summarize, and manage data. These topics will all be covered in later courses. R also has tools for file management. The focus of this lesson is on a small set of functions that you may find useful in managing your files.

### Why manage files in R?

As a data scientist, you will find it very useful to automate the management and organization of files. In the previous lesson, you learned about the power of the Terminal to run commands that allow you to more efficiently manage files than standard clicking and typing. However, for some tasks with larger scale data projects, it will be easier to work with files programatically in R rather than at the Terminal. Why? Because R is programming language, you will be able to manage files in complex situations where your actions are dependent on lot of other information. For example, if you are working with hundreds of different files, moving them to a location that depends on information in the files is much easier with a programming language such as R rather than at the Terminal. Also, in order to completely document your work in going from raw files to finished products, a good approach is to combine your data work in R (to be covered in later courses) with your file organization work in R.

### Navigating to R in RStudio Cloud

When you open a project in RStudio Cloud, you will see a Console pane that is immediately next to the Terminal pane. Usually this pane is automatically open when you open a project. The `>` that you see in the R console is called the **R prompt**. It is analogous to the Terminal prompt in that it is where you can type and enter R commands.

![Locating the Console in RStudio Cloud](images/10_fileorganization_nav_R/10_fileorganization_nav_R-1.png)

### Outline

- What is R
  - Why navigate files in R?
  - Point out we'll learn a ton more later
- Show where to get to R
- Point out main navigation commands
  - setwd()
  - getwd()
  - list.files()
  - file.rename()
  - file.create()
  - file.remove()
  - file.copy()
  - file.exists()



### Additional Resources



### Slides and Video

![Managing files in R](Update Link)

* [Slides](https://docs.google.com/presentation/d/1T_KaKPNffgoHSOqM65c_E5AI93KK2BYRBhJNXjOxRmc/edit?usp=sharing)


{quiz, id: quiz_10_nav_terminal}

### Managing files in R quiz


{/quiz}
