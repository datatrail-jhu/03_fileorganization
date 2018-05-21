# How to Work

### Why organize?

In the previous lessons we learned about how to organize our files into folders and how to name our files and folders. Doing this has the following benefits:

- Easier collaboration: You will see that as a data scientist, you will have to work with teams of other data scientists most of the time. Organizing makes collaboration a lot easier.

- Lower likelihood of making mistakes: When you organize, it is easier for you and others to see where you might have made a mistake before it's too late. 

- Easier recall: Going back to your analysis and understanding what you have done in 6 months or a year or even later will be a lot easier. If your project is not organized, it is very likely that you go back to your analysis and do not understand what you or your collaborator have previously done.

- More transparency and honesty on your part: This is because you make it easier for others to go through your files and replicate your analysis.

Using the *raw_data* folder for keeping the raw data untouched is important especially if you don't have a second copy of the raw data. If you make changes to and tidy up the raw data within your analysis, make sure you do not overwrite your raw data. It is important that you keep the raw data intact and instead add the cleaned and tidy data to the *tidy_data* folder. 

Next is using the *raw_code* folder for keeping your preliminary code. Let's see what we mean by that. When you are doing the preliminary part of your analysis, code with not constraint, that is do not worry much about how nice your code looks or whether they are self explanatory. Don't devote much of your brain power to commenting or tidying at first. Save this kind of code in the *raw_code* folder since it's raw and most of the time no one but you understands it. Later on, when you clean your code and make it more understandable, you can save bits and pieces of it in your final code file in the *final_code* folder.

### The README File

Once you have a file structure in place, write a README file that explains how code and are organized and how they are related. In other words, what is what. For each filename, we recommend to have a short description of what the file is for. You can also have a description of how the data were obtained or collected including links or references to publication or other documentation. Mention people involved with the project, and provide contact information of at least one of the collaborators.

A more detailed README file includes a list of variables, units of measurement of each variable, definition of code and symbols used to deal with missing data, Licenses or restrictions on the content of the project including the data, and information about how others should cite your analysis.


### Using comments

Our next piece of advise is that use comments within your code. Commenting in R is done by adding the pound sign (#). If you add the pound sign in the beginning of each file, R will not read that line as code and will instead skip it. So you can add your explanations about each chunk of code using the pound sign. This is an example of commenting:

```r
# calculates the products of a vector and a matrix
# checks if they can be multipled first
function (x, y){
    if (dim(x)[2] != length(y)) {
        stop("Can't multiply matrix%*%vector because the dimensions are wrong")
    }
    product <- matrix %*% vector
    return(product)
}
```

Note that the first line describes what the function does. Commenting is helpful especially when the code is more complicated and harder to understand. Keep comments short and informative and avoid inserting comments for code that have an obvious purpose, i.e. don't add comment for a line of code that adds two variables). 

### Version control

Always make sure your changes are saved and even more importantly that all your files are version controlled. Version control is common practice in data science. Don't worry if you don't know much about it. In the course that follows, we'll learn everything version control. 

### Write in a Modular Way

One mistake in writing code is to have everything in one file. This is bad practice since fixing bugs and replicating the analysis would be much harder. Therefore, it is recommended that you write code in a modular way so that each group of code that do similar things can be put in a single file and the master file calls these individual files. The result is a much cleaner and shorter master file.

### Moving to the final version

Within a folder, have your file numbering system to distinguish the files. You could use something like `data_cleaning_v001.R`. Write a final report in Rmarkdown that you can send to others. As we saw, rmd files are great tools for having a combination of code and text that you can share with others and can be run to reproduce your results. As you move along to the final version, make sure you keep updating the README file for any changes to your files and filenames. 

Budget about 20% of your time keeping track of a bulleted list of the things that you need to do and the things that you do day to day across all your data science projects. This is to help you organize and remember what you did when for future references. There are various tools for keeping track of your projects. One of them is [Benchling](https://benchling.com/). Benchling can be used for workflow management and tracking your project in a collaborative way. Check it out and give it a try.

  
### Slides and Video

![How To Work](https://www.youtube.com/watch?v=x_ywQ2sV5kc)

* [Slides](https://docs.google.com/presentation/d/1vn8Lb8YNvo1zha7GmJMlQSBRSAryRms6xy5HUtafH2A/edit?usp=sharing)  



### How to Work Quiz

{quiz, id: quiz_09_how_to_work}

? Why is file organization important?
A) All answers are correct.
b) It will be easier to replicate an analysis.
c) It will be easier to redo the analysis in future.
d) It will be easier to collaborate with others.

? What kind of information is recommended to be included in the README file of your data science project?
a) How to cite your analysis.
b) Name of the collaborators on the project.
c) File structure and how files are related.
D) All answers are correct.

? What is NOT a characteristic of a good comment within a code file in R?
a) It is concise.
b) It is informative.
C) It mentions who wrote the chunk of code that follows.
d) It follows the pound key.

{/quiz}}

