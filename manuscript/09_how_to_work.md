# How to Work

### Why Organize?

In the previous lessons we learned about how to organize our files into folders and how to name our files and folders. Doing this has the following benefits:

- Easier collaboration: You will see that as a data scientist, you will have to work with teams of other data scientists most of the time. Organizing makes collaboration a lot easier.

- Lower likelihood of making mistakes: When you organize, it is easier for you and others to see where you might have made a mistake before it's too late. 

- Easier recall: Going back to your analysis and understanding what you have done in 6 months or a year or even later will be a lot easier. If your project is not organized, it is very likely that you go back to your analysis and do not understand what you or your collaborator have previously done.

- More transparency and honesty on your part: This is because you make it easier for others to go through your files and replicate your analysis.

Using the *raw_data* folder for keeping the raw data untouched is important especially if you don't have a second copy of the raw data. If you make changes to and tidy up the raw data within your analysis, make sure you do not overwrite your raw data. It is important that you keep the raw data intact and instead add the cleaned and tidy data to the *tidy_data* folder. 

Next is using the *raw_code* folder for keeping your preliminary code. Let's see what we mean by that. When you are doing the preliminary part of your analysis, code without any constraint, that is do not worry much about how nice your code looks or whether it is self-explanatory. Don't devote much of your brain power to commenting or tidying at first. Save this kind of code in the *raw_code* folder since it's raw and most of the time no one but you understands it. Later on, when you clean your code and make it more understandable, you can save bits and pieces of it in your final code file in the *final_code* folder.

### The README File

Once you have a file structure in place, write a README file that explains how code and data are organized and how they are related. In other words, what is what. For each filename, we recommend to have a short description of what the file is for. You can also have a description of how the data were obtained or collected including links or references to publication or other documentation. Mention people involved with the project, and provide contact information of at least one of the collaborators.

A good idea is to update the README file as you work. As you create new files and folders, add their descriptions to the README file so you can keep track of what you are working on. 

You might also make a more detailed README file, which includes a list of variables, units of measurement of each variable, definition of code and symbols used to deal with missing data, Licenses or restrictions on the content of the project including the data, and information about how others should cite your analysis.


### Using Comments

Our next piece of advice is that use comments within your code. Commenting in R is done by adding the pound sign (#). If you add the pound sign at the beginning of each line, R will not read that line as code and will instead skip it. So you can add your explanations about each chunk of code using the pound sign. This is an example of commenting:

```r
# calculates the products of a vector and a matrix
# checks if they can be multiplied first
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

Always make sure your changes are saved and even more importantly that all your files are version controlled. Version control is common practice in data science. Don't worry if you don't know much about it. In a future course we'll cover version control in much more detail. 

### Write in a Modular Way

One mistake in writing code is to have everything in one file. This is bad practice since fixing bugs and replicating the analysis would be much harder. Therefore, it is recommended that you write code in a modular way so that each group of code that do similar things can be put in a single file and the master file calls these individual files. The result is a much cleaner and shorter master file.

### Draft and Final Versions

When working on a data science project you will start with data in the `data/raw_data` folder and you will start with code in the `code/raw_code` folder. Most of your early analysis will be done within the `code/raw_code` folder. When you are first starting out on a project it makes sense to work quickly, exploring a data set or a problem and figuring out what is going on. Don't worry about the details at this stage! The goal is to just try to figure out what is going on with the data you are working on. 

Within your `code/raw_code` folder you can try to have a numbering system as we described in the file naming section. You might create a file called `00_first_analysis.R` and start doing some analysis that might be messy or incomplete. You would keep track of what you working on in your README file or in a lab notebook at regular intervals. 

Once you have figured things out and know what analysis you want to do you will go back through and take pieces of the analysis and code you created in the `code/raw_code` folder, clean it up, and put it into final documents that go into the `code/final_code` and `products/writing` folders. That way you have a record of every messy analysis you did, but you also have a nice cleaned up version that you can share with other people. 

The key take home message is that you should start fast, trying out things and not being afraid to make mistakes. This is what will go in your raw folders. Then, once you have figured out what you want to do more clearly, you will make final versions that are clear and easier to communicate. 

Budget about 20% of your time keeping track of a bulleted list of the things that you need to do and the things that you do day to day across all your data science projects. This is to help you organize and remember what you did when for future references. There are various tools for keeping track of your projects. One of them is [Benchling](https://benchling.com/). Benchling can be used for workflow management and tracking your project in a collaborative way. 

  
### Slides and Video

![How To Work](https://www.youtube.com/watch?v=kKXOHJRZGdE)

* [Slides](https://docs.google.com/presentation/d/1vn8Lb8YNvo1zha7GmJMlQSBRSAryRms6xy5HUtafH2A/edit?usp=sharing)  


{quiz, id: quiz_09_how_to_work}

### How to Work quiz

?1 Why is file organization important?

A) All answers are correct.
b) It will be easier to replicate an analysis.
c) It will be easier to redo the analysis in future.
d) It will be easier to collaborate with others.

{choose-answers:4}
?1 Which of the following explains why file organization is important?

C) It will be easier for someone else to replicate your analysis.
m) All answers are correct.
o) It makes it more difficult for others to steal your analysis.
o) It makes it more difficult for others to figure out your mistakes.
o) It increases security of your data.
o) It allows data to be anonymized. 

{choose-answers:4}
?1 Which of the following explains why file organization is important?

C) It will be easier for you to redo the analysis in future.
m) All answers are correct.
o) It makes it more difficult for others to steal your analysis.
o) It makes it more difficult for others to figure out your mistakes.
o) It increases security of your data.
o) It allows data to be anonymized. 

{choose-answers:4}
?1 Which of the following explains why file organization is important?

C) It will be easier to collaborate with others.
m) All answers are correct.
o) It makes it more difficult for others to steal your analysis.
o) It makes it more difficult for others to figure out your mistakes.
o) It increases security of your data.
o) It allows data to be anonymized. 

?2 What kind of information is recommended to be included in the README file of your data science project?

a) How to cite your analysis.
b) Name of the collaborators on the project.
c) File structure and how files are related.
D) All answers are correct.

{choose-answers: 4}
?3 What is NOT a characteristic of a good comment within a code file in R?

C) It mentions who wrote the chunk of code that follows.
C) The comment includes code that must run.
o) It is concise.
o) It is informative.
o) It follows the pound key.
o) It helps explain what the code is doing

{/quiz}

