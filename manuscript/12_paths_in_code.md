# Using Paths in Code

Now that you know what a file path is and how to navigate to different directories using both the Terminal and the R Console, we'll discuss how to include file paths when coding.

### Relative and absolute paths 

Relative and absolute paths were discussed in an earlier lesson in this course. To review *very* briefly here:

#### Relative paths

**Relative paths** give a path to the destination folder based on where you are right now (your current working directory). 

![relative paths](images/12_paths_in_code/12_fileorganization_paths_in_code-2.png)

#### Absolute paths

**Absolute paths** give a path to the destination folder based on the root directory of a file system. 

![absolute paths](images/12_paths_in_code/12_fileorganization_paths_in_code-3.png)


#### Directions analogy

So, to return to analogy of giving someone directions. Imagine that your friend plans to go from the town square, then to the library, and finally to the bakery. In this analogy, the town square represents the root directory, a universal starting location.

If your friend is *currently* at the library and asks you for directions, you would likely tell them how to go from the library (where they are) to the bakery (where they want to go). This represents a **relative path** -- taking you from where you are currently to where you want to be. Alternatively, you could give them directions from the Town square, to the library, and then to the bakery. This represents an **absolute path**, directions that will always work in this town, no matter where you are currently, but that contain extra information given where your friend is currently.

![Directions and paths analogy](images/12_paths_in_code/12_fileorganization_paths_in_code-4.png)

### Paths in projects

In this course, you've learned how to organize your project folders and name your files for every data science project you complete. Setting up projects in this way not only helps keep you organized and your file naming consistent, but it also sets you up to easily refer to many different files while you're writing code.

Often you'll find yourself writing some code in your `raw_code` folder, but you'll want to read in some data that are in your `raw_data` folder. The good thing is that since everything for this project is together in a subfolders within a single project folder, you can accomplish this easily. 

#### Use relative paths in projects

To easily reference back to a dataset in your `raw_data` folder where you have a file called `dataset.csv`, you'll want to use a relative path. You'll set your path relative to the project folder. In this example, you will have set your project directory as `/cloud/directory` and you would reference your **relative path** `data/dataset.csv`. 

![relative path to dataset.csv](images/12_paths_in_code/12_fileorganization_paths_in_code-6.png)

Since you've already defined where your starting point is for this project (`/cloud/directory`), you'll be able to and should refer to every folder and every file easily with relative paths.

#### Relative paths make sharing projects easier

The reason relative paths for each project are the correct approach is because if you share this project with someone else with a different computer, you would likely share the project file and all the subdirectories. If you were to share this with someone else and relative paths were used throughout all the code in your project, that new person would be able to follow along and run all your code without any problems.

![Using relative paths enables sharing](images/12_paths_in_code/12_fileorganization_paths_in_code-7.png)

However, you are *not* likely to (and shouldn't!) share all the contents of your entire computer with another person. If you had used absolute paths that work for your computer, rather than relative paths, none of the paths will make any sense on the person you've shared with's computer. To enable sharing with someone else, you should always use relative paths in your code that are relative to the project folder. Thankfully, there's an easy way in R to make that happen! 

![Absolute paths prohibit sharing](images/12_paths_in_code/12_fileorganization_paths_in_code-8.png)

### The `here` package  

We haven't yet discussed what an R package is or what the basic commands in R are. However, we have covered file organization at this point *and* how to navigate within R. With that knowledge, we're now going to discuss how to use the here package. 

While we'll define in more depth what packages are, at this point, think of packages as something that allows you to accomplish something that you wouldn't have been able to otherwise or that wouldn't have been as easy to accmomplish without the package. 

We're going to discuss using a single R package now, called [`here`](https://github.com/r-lib/here). 

To get started using the `here` package (or any R package!), it first has to be installed (using the `install.packages()` function) and then loaded in (using the `library()` function). The code to copy and paste into your R console is below:

```r
install.packages("here")
library(here)
```

### Why to use `here`

Okay, so if we're discussing packages later, why discuss this *one* package now? Well, `here` is a package specifically designed to help you deal with file organization when you're coding.  

This package allows you to define in which folder all your relative paths should beging within a project.

#### Setting your project directory

After installing and loading the `here` package, to set your project directory using `here()`, you'll simply type the command `here()`. You'll notice that the output of `here()` and `getwd()` in this case is the same; however, what they're doing behind the scenes is different. 

* `getwd()` - takes you to the directory you are in currently
* `here()` - sets the directory to use for all future relative paths

The `here()` function is what you want to use to set your project directory so that you can use it for future relative paths in your code. While in this case it *also* happened to be in the same directory you were in, it doesn't have to be. The here() function looks to see if you have a .Rproj file in your project. If then sets your base directory to whichever directory that file is located. 

![here() sets your project directory for future reference using here()](images/12_paths_in_code/12_fileorganization_paths_in_code-10.png)

So, if we were to change our current directory and re-type `here()` in the Console, you'll note that the output from here() does not change because it's still looking for the directory where .Rproj is. 


![here() does not care what your current working directory is](images/12_paths_in_code/12_fileorganization_paths_in_code-11.png)

Note: In cases where there is no .Rproj file, `here()` will look for files other than a .Rproj file. You can read about those cases in the fine print [here](https://github.com/jennybc/here_here#the-fine-print). But for most of your purposes, `here()` will behave as we just discussed.


#### Get files paths using `here()`

After setting your project folder using `here()`, R will then know what folder to use to define any and all other paths within this project.

For example, if you wanted to include a path to a file named "intro_code.R" in your `raw_code` directory, you would simply specify that in your code like this:

```r
here("code", "raw_code", "intro_code.R")
```

This code says start from where I've already defined the project starts (`here()`), then look in the folders `code` and then `raw_code`, for the file "intro_code.R."

The syntax is simplified when using `here()`. Each subdirectory or file in the path is in quotes and simply separated by commas within the `here()` function, and voila you have the relative path you're looking for relative to `here()`.

The output from this code includes the correct file path to this file, just as you wanted!

![using here to get a file path](images/12_paths_in_code/12_fileorganization_paths_in_code-2.png)


#### Where you should use this

You should use `here()` to set the base project directory for each data science project you do. And, you should use relative paths using `here()` throughout your code any time you want to refer to a different directory or sub-directory within your project using the syntax we just discussed. 

### Additional Resources

[here, here](https://github.com/jennybc/here_here), by [Jenny Bryan](https://www.stat.ubc.ca/~jenny/)
[here documentation](https://github.com/r-lib/here), by [Kirill Müller](https://github.com/krlmlr)

### Slides and Video

![Coding with Paths](Update Link)

* [Slides](https://docs.google.com/presentation/d/18hkG4zMtlD5c6RUC2yzKG90sl1_zMT3b6D84qGvR1mQ/edit?usp=sharing)


{quiz, id: quiz_12_coding_with_paths}

### Using paths in code quiz

Refer to this diagram to answer the quiz questions below. Assume "cloud" is the root directory for your computer.

![Directory structure](images/12_paths_in_code/12_fileorganization_paths_in_code-1.png)

{choose-answers: 4}

?  "/cloud/project/data/tidy_data"" is an example of a(n):

C) absolute path that directs you to the folder tidy_data
m) relative path that directs you to the folder tidy_data
o) absolute path that directs you to the folder raw_data
o) relative path that directs you to the folder raw_data
o) absolute path that directs you to the folder data
o) relative path that directs you to the folder data
o) distinct path that directs you to the folder tidy_data
o) suggestive path that directs you to the folder tidy_data

{choose-answers: 4}

?  How would you use the here() function to specify the path to a script called "script.R" in final_code file?

C) here("code", "final_code", "script.R")
o) here("code", "/" , "final_code", "/", "script.R")
o) here("code", "/" , "final_code", "/")
o) here("code", "final_code")
o) "code/final_code/script.R"
o) here("code", "code", "script.R")
o) here("code", "/" , "code", "/", "script.R")
o) here("code", "/" , "code", "/")
o) here("code", "code")
o) "code/code/script.R"

{choose-answers: 4}

?  Assuming your current working direcotry is "/cloud/project", hich of the following is an example of a relative path directing you to the folder "data/tidy_data"?

C) data/tidy_data
m) /cloud/project/data/tidy_data
o) data/raw_data
o) here(tidy_data)
o) here("tidy_data")
o) tidy_data
o) /cloud/data/tidy_data


{/quiz}