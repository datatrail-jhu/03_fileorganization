# Navigating in the Terminal

As was discussed in the first lesson of this course, one of the most important aspects of being a productive data scientist is staying organized. And a big part of staying organized is in knowing where your files are located. In these next few lessons, we will be getting you fluent in orienting yourself in file systems in two areas: the Terminal and R/RStudio. In this lesson, we will focus on working with the Terminal.

## What is the Terminal?

The Terminal is an interface to the operating system of a computer. That is, it provides a way for you to type commands in order to perform actions on a computer. For example, there are commands to create new files and folders and to open files and folders. On your Chromebook, you are familiar with using your mouse to perform such actions. When you are working with data on RStudio Cloud, however, you will not be able to use your mouse for everything that you'll want to do. It will be important to become comfortable with the idea of a Terminal as a place for purely text-based commands. In RStudio Cloud, the Terminal is located in the tab next to the Console.

![Locating the Terminal in RStudio Cloud](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-1.png)

When you click on this tab, you will see a pane that looks as follows:

![The Terminal prompt](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-2.png)

You will always see a string of text at the beginning of the line. This is called the **Terminal prompt**. To the right of the dollar sign, you will be entering your commands. The Terminal is going to be extremely important in the next course when you learn about version control systems and GitHub because it is the primary interface for working with those tools.

## Why do we need to navigate in the Terminal?

To better understand why we need to learn about commands for navigating in the Terminal, let's take a look again at the folder structure/directory structure that you created earlier in this course. Within a project folder, it is recommended that you set up the folders within as follows:

![Directory structure](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-3.png)

In future courses, whenever you write code and run commands within R to work with data, or whenever you use Git commands to document updates to your files, you will be working *in a particular location*. To know your location within a file system is to know exactly what folder you are in right now. For example, you may currently be working on preliminary versions of R code within the `raw_code` subdirectory. You are *in* the `raw_code` subdirectory. Knowing this is important because if you want to tell Terminal to perform some actions on files in other folders, you will need to be able to tell the Terminal where that folder is. That is, you will need to be able to specify a **path** to that folder. A path is a string that specifies a sequence of folders to traverse to end up at a final destination. For example, you may wish to navigate to the `exploratory` subfolder within the `figures` folder to see what graphics you've created. There are two ways to specify that location. You can specify a path to that folder based on where you are right now (in `raw_code`). A path that is relative to a particular folder is called a **relative path**.

![Relative path](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-4.png)

Alternatively, you can specify a path to that folder based on starting from the **root directory** of the file system. The root directory of a file system is specified with a single forward slash `/` and is special in that it cannot be contained within other folders. In this file system, the root directory contains only one folder `cloud`. A path that begins with a forward slash is an **absolute path**; it starts at the root directory.

![Absolute path](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-5.png)

**Analogy**: The root directory is analogous to a town square, a universal starting location. The desired destination location might be the baker. An absolute path specifies how to reach the bakery starting from this universal starting location of the town square. However, if we are in the library right now, a relative path would specify how to reach the bakery from our current location in the library. This could be pretty different than the path from the town square. We will be discussing both absolute and relative paths throughout this lesson.

## Important commands

Let's get familiar with essential commands for performing certain actions in the Terminal.

### Where am I right now?

If you want to know where you are (what folder you are in), you can use the `pwd` command by typing `pwd` at the Terminal prompt and hitting Enter. This stands for "print working directory", and it prints the absolute path to your current location. In the example below we are in the `project` folder within the `cloud` folder. We can determine that this is an absolute path because it starts with a forward slash `/`.

![pwd command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-7.png)

### What is in this folder?

If you want to know what files and folders are contained within your current directory, you can use the `ls` command. This stands for "list", and it lists the files and folders within the current directory. If you just use the `ls` command without any options, the contents will be displayed horizontally across lines. If you add the `-lh` option with a space after the initial `ls` command, the output is displayed more nicely. The `l` part displays the results in a longer form with more information than just the file name. The `h` part displays the file sizes in a human-readable format. The most important pieces of information are in the last three columns, which display the file or folder size, the date the file or folder was last modified, and the name of the file or folder. You can also list the contents of a specific folder by specifying an absolute or relative path after the main `ls` command. In the example below, we list the contents of the `products` subfolder using a relative path.

![ls command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-8.png)

### Change directory

If you would like to change your current working folder, you can use the `cd` command. This stands for "change directory" and moves you to the folder that you specify with a path after `cd`. If I want to move to the `raw_data` folder, I can specify this with a relative path `data/raw_data/` because I am currently in the `cloud/project/` folder. When you type these paths, it will be incredibly useful to use the **tab completion** feature of Terminal. With tab completion, you can partially type part of a folder or file name and hit tab to automatically fill in the remainder of the name. So here I can type `cd da`, and when I hit tab, this will automatically complete to `cd data/` because there are no other files or folders in this folder that start with `da`. From here I can type `cd data/r` and hit tab to automatically fill in the complete command `cd data/raw_data/`. Try this out when you're typing at the Terminal prompt - it will save you a lot of time!

![cd command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-9.png)

I could also have specified an absolute path with `cd /cloud/project/data/raw_data/`. In this case, because of my initial working directory, both the relative and absolute paths take me to the same folder. Note that we have checked our updated working directory with the `pwd` command. Note that this path also happens to match the part of the Terminal prompt just before the dollar sign. This is a way to doubly verify where you are within the file system.

![cd command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-10.png)

If you try to change directory to a nonexistent folder, you will get an error message that looks as below:

![Error with the cd command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-11.png)

#### Absolute vs. relative paths

Let's go a little bit further with exploring the difference between absolute and relative paths. Let's say that I have some code in the `raw_code` folder, and in that code, I want to create some exploratory graphics in the `exploratory` folder. Using our file system on RStudio Cloud, the path to the `exploratory` folder could be specified with the absolute path `/cloud/project/figures/exploratory/`. However, if someone else copies over the four main folders (`data`, `code`, `figures`, and `products`) onto their own computer and puts them inside folders with different names, this absolute path will not work. This person has the `root` and `work` folders instead of the `cloud` and `project` folders.

![Absolute paths are not portable](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-12.png)

Rather than using an absolute path, a robust way to specify the path to the `exploratory` folder is with a relative path. In this way, our code will work on all computers, which is essential for data science work. Specifying this relative path is a little more complicated than we have seen earlier because we have to traverse up through some folders that contain our current working directory and down through another set of folders. To specify the folder containing the current working directory, we use `../`. When we are in the `raw_code` folder, the `../` specifies the `code` folder because it is the one directly containing our current directory. However, to enter the `figures` folder, we need to go up one more level to the folder that contains the `code` folder. On RStudio Cloud, this is the `project` folder, but for this other person, it is the `work` folder. We can go "up" one more folder level with another `../`. So the complete relative path from `raw_code` to `exploratory` is `../../figures/exploratory/`.

![Relative vs absolute paths](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-13.png)

Let's look at one more example to reinforce these ideas. Our current working directory is the `raw_code` directory. We want to specify a path to the `final_code` directory. There are several ways to do acheive this, but the first listed below is the most straightforward.

- `../final_code/`
- `../../code/final_code/`
- `../../../work/code/final_code/`

![Additional example for relative paths](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-14.png)

### Cycling through previous commands

Often when working in the Terminal, you will want to run the same or similar commands that you have run earlier. For example, you may want to change directories, list files, and then repeat this process as you change to other directories. You can avoid typing commands over and over by using the up and down arrow keys at the Terminal prompt. Hitting the up arrow key pulls up the last command that you entered. You can keep hitting up and down to cycle through your previous commands.

### The wildcard operator

In several different Terminal commands, it can be useful to specify only part of a file or folder name. For example, if we go to the `raw_code` folder and use the `ls` command, we see that there are 4 files. In larger projects, there may be many more files and we might not want to view all of them. We can specify certain patterns of files to list after the main `ls` command using part of the file name combined with the `*` wildcard operator. This operator matches any number of characters. So to list only files that start with "clean", we can use `ls -lh clean*`. To only list files that contain "dataset1", we can use `ls -lh *dataset1*` to match any characters on either side of the "dataset1" pattern. This will be useful when you work more with GitHub, starting in the next course.

![Wildcard operator](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-16.png)

## Summary

The Terminal is an interface to the operating system of a computer that you will mainly be using for interfacing with GitHub, which will be covered in the next course. The essentials of working with the Terminal include knowing exactly what folder you are in with the `pwd` command, changing folders with the `cd` command, and listing files with the `ls` command. When you work with Git commands in the next course, you will mostly be using the Terminal to navigate to the correct working directory and using Git commands to track changes you make in specified files. In order to specify those files, you will need to be comfortable with entering relative paths, as we covered in this lesson. Because Git commands allow use of the `*` wildcard operator, it will be useful for you to become comfortable with "testing" your syntax of specifying files with the `ls` command. That is, you can play with the wildcards and their placement using the `ls` command to make sure the correct files are listed. Then you can use the same pattern to specify those files in a Git command.


## Original lesson outline

- What is the terminal
  - Explain how to get to it in rstudio
  - Point out we'll learn a lot more later
- Why navigate in the terminal?
- Important commands
  - cd
  - ls
  - pwd
  - *
  - .
  - -r 
  - rm
  - touch
  - cp
  - mv
- How does this work with file naming
  - globs
- How do you write about where files are
  - show standard notation
  - translate notation to navigation commands


### Slides and Video

* [Slides](https://docs.google.com/presentation/d/18PSP0OXbduVX_qjWX87zTxyNj6OaX5pU9Sw2f83NGDY/edit?usp=sharing)


{quiz, id: quiz_10_nav_terminal}

### Navigating in the Terminal quiz

{choose-answers: 4}
? Refer to the following diagram of a file system for this question. The current working directory is the `final_code` directory. Which of the following is a correct relative path to the `explanatory` directory?

![Directory structure](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-3.png)

C) `../../figures/explanatory`
C) `../../../project/figures/explanatory`
o) `/cloud/project/figures/explanatory/`
o) `cloud/project/figures/explanatory/`
o) `../figures/explanatory`
o) `figures/explanatory`
o) `/figures/explanatory`
o) `../project/figures/explanatory`
o) `project/figures/explanatory`

{choose-answers: 4}
? Refer to the following diagram of a file system for this question. The current working directory is the `final_code` directory. Which of the following is a correct absolute path to the `explanatory` directory?

![Directory structure](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-3.png)

C) `/cloud/project/figures/explanatory/`
o) `../../figures/explanatory`
o) `../../../project/figures/explanatory`
o) `cloud/project/figures/explanatory/`
o) `../figures/explanatory`
o) `figures/explanatory`
o) `/figures/explanatory`
o) `../project/figures/explanatory`
o) `project/figures/explanatory`

{choose-answers: 4}
? How can you determine the current working directory in the Terminal in RStudio?

C) Look at the path displayed before the dollar sign at the prompt
C) `pwd`
o) `ls`
o) `ls -lh`
o) `cd`
o) `cd /`

{choose-answers: 7}
? In my current working directory, I have two folders called `explanatory` and `exploratory`. I want to change my working directory to the `exploratory` folder. What is the earliest point in the typing of my command where I can hit the tab key to automatically complete the file name?

C) `cd explo`, then hit tab key
m) `cd e`, then hit tab key
m) `cd ex`, then hit tab key
m) `cd exp`, then hit tab key
m) `cd expl`, then hit tab key
o) `cd explor`, then hit tab key
o) `cd explora`, then hit tab key
o) `cd explorat`, then hit tab key
o) `cd explorato`, then hit tab key
o) `cd explorator`, then hit tab key
o) `cd exploratory`, tab completion won't save time here.

{choose-answers: 4}
? Which of the following commands displays only the files in the current working directory that have a `.txt` extension?

C) `ls *.txt`
C) `ls -lh *.txt`
o) `ls .txt`
o) `ls -lh .txt`
o) `ls .txt*`
o) `ls -lh .txt*`

{/quiz}
