# Managing files in the Terminal

As was discussed in the first lesson of this course, one of the most important aspects of being a productive data scientist is staying organized. And a big part of staying organized is in managing your files: knowing where they are located and manipulating them with ease. In these next few lessons, we will be getting you fluent in orienting yourself in file systems in two areas: the Terminal and R/RStudio. In this lesson, we will focus on working with the Terminal.

### What is the Terminal?

The Terminal is an interface to the operating system of a computer. That is, it provides a way for you to type commands in order to perform actions on a computer. For example, there are commands to create new files and folders and to open files and folders. On your Chromebook, you are familiar with using your mouse to perform such actions. When you are working with data on RStudio Cloud, however, you will not be able to use your mouse for everything that you'll want to do. It will be important for you to become comfortable with using the Terminal as a place for purely text-based commands. In RStudio Cloud, the Terminal is located in the tab next to the Console.

![Locating the Terminal in RStudio Cloud](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-1.png)

When you click on this tab, you will see a pane that looks as follows:

![The Terminal prompt](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-2.png)

You will always see a string of text at the beginning of the line. This is called the **Terminal prompt**. To the right of the dollar sign, you will be entering your commands. The Terminal is going to be extremely important for efficient management of your files. You will also use it extensively in the next course when you learn about version control systems and GitHub because it is the primary interface for working with those tools.

### Why manage files in the Terminal?

As we've discussed, the Terminal is a command-based interface to a computer operating system. This turns out to be a very flexible and fast way to manage your files once you become comfortable with a few commands. Let's say that you wanted to make a copy of a folder. Whether on RStudio Cloud or on Google Drive, you would need to go through a series of clicks and typing to find that folder, copy it, and rename it. Within the Terminal, this can all be acheived with a single command.

### File system example and vocabulary

To set up an example of a file system that we'll be using throughout this lesson, let's take a look again at the folder structure/directory structure that you created earlier in this course. Within a project folder, it is recommended that you set up the folders within as below. We will be working with this directory setup in an RStudio Cloud project.

![Directory structure](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-4.png)

In future courses, whenever you write code and run commands within R to work with data, or whenever you use Git commands to document updates to your files, you will be working *in a particular location*. To know your location within a file system is to know exactly what folder you are in right now. The folder that you are in right now is called the **working directory**. Your current working directory in the Terminal may be different from your current working directory in R and may yet even be different from the folder shown in the Files pane of RStudio. The focus of this lesson is on the Terminal, so we will not discuss working directories within R until the next lesson.

Knowing your working directory is important because if you want to tell Terminal to perform some actions on files in other folders, you will need to be able to tell the Terminal where that folder is. That is, you will need to be able to specify a **path** to that folder. A path is a string that specifies a sequence of folders to traverse in order to end up at a final destination. The end of a path string may be a file name if you are creating a path to a file. If you are creating a path to a folder, the path string will end with the destination folder. In a path, folder names are separated by forward slashes `/`. For example, let's say that your current working directory in the Terminal is the `raw_code` directory, and you wish to navigate to the `exploratory` subfolder within the `figures` folder to see the graphics you've created.

![Definitions: working directory and path](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-5.png)

There are two types of paths that can lead to that location. The first is called a **relative path** which gives a path to the destination folder based on where you are right now (in `raw_code`). A little later in this lesson you'll learn how to construct relative paths.

![Relative path](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-6.png)

Alternatively, you can specify an **absolute path**. An absolute path starts at the **root directory** of a file system. The root directory does not have a name like other folders do. It is specified with a single forward slash `/` and is special in that it cannot be contained within other folders. In the current file system, the root directory contains a folder called `cloud`, which contains a folder called `project`. This `project` folder contains the four main folders that you learned about in a previous lesson.  A little later in this lesson you'll learn how to construct absolute paths.

![Absolute path](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-7.png)

**Analogy**: The root directory is analogous to a town square, a universal starting location. The desired destination location might be the baker. An absolute path specifies how to reach the bakery starting from this universal starting location of the town square. However, if we are in the library right now, a relative path would specify how to reach the bakery from our current location in the library. This could be pretty different than the path from the town square.

### Important commands

Now that you have some vocabulary, we can delve into details about creating and using paths with different Terminal commands for managing files.

#### Where am I right now?

If you want to know your current working directory with the Terminal (what folder you are in), you can use the `pwd` command by typing `pwd` at the Terminal prompt and hitting Enter. This stands for "print working directory", and it prints the absolute path to your current location. In the example below we are in the `project` folder within the `cloud` folder. We can determine that this is an absolute path because it starts with a forward slash `/`.

![pwd command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-10.png)

#### What is in this folder?

If you want to know what files and folders are contained within your current directory, you can use the `ls` command. This stands for "list", and it lists the files and folders within the current directory. If you just use the `ls` command without any options, the contents will be displayed horizontally across lines. If you add the `-lh` option with a space after the initial `ls` command, the output is displayed more nicely. The `l` part displays the results in a longer form with more information than just the file name. The `h` part displays the file sizes in a human-readable format. The most important pieces of information are in the last three columns, which display the file or folder size, the date the file or folder was last modified, and the name of the file or folder. You can also list the contents of a specific folder by specifying an absolute or relative path after the main `ls` command. In the example below, we list the contents of the `products` subfolder using a relative path.

![ls command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-11.png)

When you use `ls` without specifying any path, it displays the contents of the current working directory. You can get the same results by specifying a period `.` for the path, as shown below. The period stands for the current working directory.

![ls command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-12.png)

#### Change directory

If you would like to change your current working directory, you can use the `cd` command. This stands for "change directory" and moves you to the folder that you specify with a path after `cd`. If I want to move to the `raw_data` folder, I can specify this with a relative path `data/raw_data/` because I am currently in the `cloud/project/` folder. When you type these paths, it will be incredibly useful to use the **tab completion** feature of Terminal. With tab completion, you can partially type part of a folder or file name and hit tab to automatically fill in the remainder of the name. So here I can type `cd da`, and when I hit tab, this will automatically complete to `cd data/` because there are no other files or folders in this folder that start with `da`. From here I can type `cd data/r` and hit tab to automatically fill in the complete command `cd data/raw_data/`. Tab completion tries to fill in as much as possible but may not fill in completely if you have multiple folders that start with the same letters. If I had a folder called `dance` in the `project` folder, tab completion of `cd da` would not proceed further, but `cd dat` would. Try this out when you're typing at the Terminal prompt - it will save you a lot of time!

![cd command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-13.png)

I could also have specified an absolute path with `cd /cloud/project/data/raw_data/`. In this case, because of my initial working directory, both the relative and absolute paths take me to the same folder. Note that we have checked our updated working directory with the `pwd` command. Also note that this path matches the part of the Terminal prompt just before the dollar sign. This is a way to doubly verify where you are within the file system.

![cd command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-14.png)

If you try to change directory to a nonexistent folder, you will get an error message that looks as below:

![Error with the cd command](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-15.png)

##### Absolute vs. relative paths

Let's go a little bit further with exploring the difference between absolute and relative paths. Let's say that I have some code in the `raw_code` folder, and in that code, I want to create some exploratory graphics in the `exploratory` folder. Using our file system on RStudio Cloud, the path to the `exploratory` folder could be specified with the absolute path `/cloud/project/figures/exploratory/`. However, if someone else copies over the four main folders (`data`, `code`, `figures`, and `products`) onto their own computer and puts them inside folders with different names, this absolute path will not work. Why? Because this person happens to have the `root` and `work` folders instead of the `cloud` and `project` folders.

![Absolute paths are not portable](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-16.png)

Rather than using an absolute path, a robust way to specify the path to the `exploratory` folder is with a relative path. In this way, our code will work on all computers, which is essential for data science work. Specifying this relative path is a little more complicated than we have seen earlier because we have to traverse up through some folders that contain our current working directory and down through another set of folders. To specify the folder containing the current working directory, we use `../`. When we are in the `raw_code` folder, the `../` specifies the `code` folder because it is the one directly containing our current directory. However, to enter the `figures` folder, we need to go up one more level to the folder that contains the `code` folder. On our RStudio Cloud, this is the `project` folder, but for this other person, it is the `work` folder. We can go up one more folder level with another `../`. So the complete relative path from `raw_code` to `exploratory` is `../../figures/exploratory/`.

![Relative vs absolute paths](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-17.png)

Let's look at one more example to reinforce these ideas. Our current working directory is the `raw_code` directory. We want to specify a path to the `final_code` directory. There are several ways to do acheive this, but the first listed below is the most straightforward.

- `../final_code/`
- `../../code/final_code/`
- `../../../work/code/final_code/`

![Additional example for relative paths](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-18.png)

#### Cycling through previous commands

Often when working in the Terminal, you will want to run the same or similar commands that you have run earlier. For example, you may want to change directories, list files, and then repeat this process as you change to other directories. You can avoid typing commands over and over by using the up and down arrow keys at the Terminal prompt. Hitting the up arrow key once pulls up the last command that you entered. Hitting the up key twice pulls up the command you entered two times ago. Now hitting down will pull up your last command again. You can keep hitting up and down to cycle through your previous commands. Try this out when you are typing at the Terminal!

#### The wildcard operator

In several different Terminal commands, it can be useful to specify only part of a file or folder name. For example, if we go to the `raw_code` folder and use the `ls` command, we see that there are 4 files. In larger projects, there may be many more files and we might not want to view all of them. We can specify certain patterns of files to list after the main `ls` command using part of the file name combined with the `*` wildcard operator. This operator matches any number of characters. So to list only files that start with "clean", we can use `ls -lh clean*`. To only list files that contain "dataset1", we can use `ls -lh *dataset1*` to match any characters on either side of the "dataset1" pattern. This will be useful when you work more with GitHub, starting in the next course.

![Wildcard operator](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-20.png)

#### Copying files and folders

Copying files and folders will come up often during your work. You may want to copy a messy code file to a new file to begin cleaning it up. It may be useful to do this for an entire folder. To copy in Terminal, we can use the `cp` command. To copy one file, the syntax is

```text
cp path_to_original_file path_to_new_file
```

The path to the original file and the path to the new file can be absolute or relative paths. In the path to the new file, you can specify a different file name to rename it. In the example below, the first command `cp clean_dataset1.R ../final_code/` copies the `clean_dataset1.R` file to the `final_code` folder and keeps the same name. The second command `cp clean_dataset1.R ../final_code/clean_dataset1_renamed.R` specifies the relative path and a new file name. When we list the contents of the `final_code` folder, we see both the originally named file and the renamed file.

![Copying a single file](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-21.png)

We can combine copying with the wildcard operator to copy multiple files. This does not rename the files. We can also copy multiple files into a directory by naming the files explicitly. That is `cp analyze* ../final_code/` achieves the same as `cp analyze_dataset1.R analyze_dataset2.R ../final_code/`.

![Copying multiple files](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-22.png)

To copy a folder, we must specify the recursive option `-r` in order to copy all of the files and folders inside the one being copied. In the example below, using `cp final_code/ publication_code` doesn't work, but `cp -r final_code/ publication_code` does work. Note that a final forward slash at the end of `final_code` and `publication_code` is optional. In these examples, you will see the trailing forward slash when tab completion was used to speed up typing.

![Copying a folder](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-23.png)

#### Moving files and folders

In the process of organizing your files, you will undoubtedly need to move files and folders to different locations. To move files and folders in Terminal, we can use the `mv` command. This command also renames files and folders. Similar to the copy command, the syntax for moving one file is

```text
mv path_to_original_file path_to_new_file
```

Just as with copy, the path to the original file and the path to the new file can be absolute or relative paths. In the path to the new file, you can specify a different file name to rename it. In the example below, the first command `mv ../final_code/clean_dataset1_renamed.R .` moves the `clean_dataset1_renamed.R` file to the current working directory (indicated by the period at the end of the command) and keeps the same name. The next two commands `mv clean_dataset1.R tidy_dataset1.R` and `mv clean_dataset2.R tidy_dataset2.R` rename the files in the working directory to start with `tidy` instead of `clean`. When we list the contents of the working directory, we see both the moved file and the two renamed files.

![Moving a single file](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-24.png)

We can combine moving with the wildcard operator to move multiple files. This does not rename the files. We can also move multiple files into a directory by naming the files explicitly. This is achieved with `mv tidy_dataset1.R tidy_dataset2.R ../raw_code/`.

![Moving multiple files](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-25.png)

To move a folder into another folder, we use the same syntax for moving a single file:

```text
mv path_to_folder_being_moved destination_path
```

In the example below, we achieve this with `mv raw_code/ publication_code/`. We can also rename a folder by specifying a new name for the destination path. In the example, we achieve this with `mv publication_code/ pub_code`.

![Moving and renaming a folder](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-26.png)

#### Deleting files and folders

To delete files and folders in the Terminal, we can use the `rm` command, which stands for remove. To remove a single file, the syntax is as follows:

```text
rm path_to_file_to_delete
```

To remove multiple files, you can specify paths to multiple files separated by spaces or use the wildcard operator. Examples are shown below.

![Deleting files](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-27.png)

To delete a folder, we must specify the recursive option `-r` in order to recursively delete all of the files and folders inside the one being deleted. This is exactly as we had to do with copying a folders. In the example below, using `rm final_code/` doesn't work, but `rm -r final_code/` does work.

![Deleting a folder](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-28.png)

Be very careful when deleting files and folders because this action is irreversible! In particular, `rm *` will delete all files in the current working directory. If you are using the wildcard operator, test your wildcard pattern with an `ls` command before deleting anything.

#### Creating files and folders

To create an empty file in the Terminal, we can use the `touch` command with `touch path_to_file`. The file will be empty, but it serves as a placeholder in case you decide to later open and edit the file.

![Creating a new file](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-29.png)

To create a new directory in the Terminal, we can use the `mkdir` command, which stands for "make directory." After `mkdir`, type the path to the folder that we want to create.

![Creating a new directory](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-30.png)

### Summary

The Terminal is an interface to the operating system of a computer that you will be using to manage your files and to interface with GitHub, which will be covered in the next course. The essentials of navigating in the Terminal include knowing exactly what folder you are in with the `pwd` command and changing folders with the `cd` command. The essentials of managing files in the Terminal includes listing files with the `ls` command, copying them with `cp`, moving them with `mv`, and deleting them with `rm`. When you work with Git commands in the next course, you will be using the Terminal to navigate to the correct working directory and using Git commands to track changes you make in specified files. In order to specify those files, you will need to be comfortable with entering relative paths, as we covered in this lesson. Because Git commands allow use of the `*` wildcard operator, it will be useful for you to become comfortable with writing wildcard patterns to match multiple files. You can always test your patterns with an `ls` command to see that the desired files are being listed. To create new files, you can use the `touch` command, and to create new folders, you can use the `mkdir` command. Overall, managing your files in the Terminal will save you a lot of time in the long run compared to manual clicking.

### Additional Resources

- [The ls command](https://shapeshed.com/unix-ls/)
- [The cp command](https://shapeshed.com/unix-cp/)
- [The mv command](https://shapeshed.com/unix-mv/)
- [The rm command](https://shapeshed.com/unix-rm/)


### Slides and Video

![Managing files in the Terminal](Update Link)

* [Slides](https://docs.google.com/presentation/d/18PSP0OXbduVX_qjWX87zTxyNj6OaX5pU9Sw2f83NGDY/edit?usp=sharing)


{quiz, id: quiz_10_nav_terminal}

### Managing files in the Terminal quiz

The following diagram of a file system will be used for some of the quiz questions.

![Directory structure](images/10_fileorganization_nav_terminal/10_fileorganization_nav_terminal-4.png)

{choose-answers: 4}
? Refer to the above diagram of a file system for this question. The current working directory is the `final_code` directory. Which of the following is a correct relative path to the `explanatory` directory?

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
? Refer to the above diagram of a file system for this question. The current working directory is the `final_code` directory. Which of the following is a correct absolute path to the `explanatory` directory?

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
o) `cd exploratory`; tab completion won't save time here.

{choose-answers: 4}
? Which of the following commands displays only the files in the current working directory that have a `.txt` extension?

C) `ls *.txt`
C) `ls -lh *.txt`
o) `ls .txt`
o) `ls -lh .txt`
o) `ls .txt*`
o) `ls -lh .txt*`

{choose-answers: 4}
? Refer to the above diagram of a file system for this question. The current working directory is the `raw_data` directory. Which of the following commands will copy a file called `data.txt` in the `tidy_data` directory to the current working directory?

C) `cp ../tidy_data/data.txt .`
o) `cp ../tidy_data/data.txt`
o) `cp tidy_data/data.txt .`
o) `cp tidy_data/data.txt`
o) `mv ../tidy_data/data.txt .`
o) `mv ../tidy_data/data.txt`

{choose-answers: 4}
? Refer to the above diagram of a file system for this question. The current working directory is the `raw_data` directory. Which of the following commands will delete the `writing` directory?

C) `rm -r ../../products/writing`
o) `rm ../products/writing`
o) `rm ../../products/writing`
o) `rm ../../../products/writing`
o) `rm -r ../products/writing`
o) `rm -r ../../../products/writing`

{choose-answers: 4}
? Refer to the above diagram of a file system for this question. The current working directory is the `raw_code` directory. This directory contains 4 files: `tidy1.R`, `tidy2.R`, `trim1.R`, `trim2.R`. Which of the following commands will move only the `tidy1.R` and `tidy2.R` files out of this directory and into the `final_code` directory?

C) `mv tidy1.R tidy2.R ../final_code/`
C) `mv tidy*.R ../final_code/`
C) `mv tidy* ../final_code/`
C) `mv tid* ../final_code/`
C) `mv ti* ../final_code/`
o) `mv t* ../final_code/`
o) `cp tidy1.R tidy2.R ../final_code/`
o) `cp tidy* ../final_code/`
o) `mv tidy*.R ../../final_code/`
o) `mv tidy* ../../final_code/`
o) `mv tidy*.R final_code/`
o) `mv tidy* final_code/`

{/quiz}
