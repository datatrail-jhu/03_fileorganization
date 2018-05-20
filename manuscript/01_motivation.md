{
course-completeness: 100
course-attempts: 2
default-quiz-attempts: 2
default-random-choice-order: true
}

# Motivation

Data science projects involve lots of files. There are files of data, files for code, files for documentation, figures, documents to communicate with other people. A surprising amount of doing data science really well is just being good at managing and organizing all of these files so that they are: 

* Easy to find
* Easy to share
* Easy to understand
* Easy to update

The reason that you need to make it easy to find and work with the files in your analysis is because data science is really closely related to communication. The reason we use data is to understand the world and communicate that understanding. So when you are building a data science project, you should be thinking about who will be on the receiving end of your data analysis. 

While you are actively working on a project it is often easy to find any file you need off the top of your head. But the audience of your data analysis is not you, right now. One audience is other people who you will share your work with. They don't know about all the different places you have stored data, or which piece of code to run first. You need to make it easy on them to be able to understand what you did. 

Another audience that may surprise you when you are just starting, but will be familiar to any experienced data analyst is you. A twist on a [famous saying about data science](http://kbroman.org/Tools4RR/assets/lectures/01_intro.pdf) is: 

> Your closest co-worker is you six months ago, but you don't reply to emails. 

This is because it is really common for you to work on a data science project, present the results, and then move on to another project. But someone else is studying your results and might have questions and want you to make a change. So a few months later, when you've forgotten where everything is, they come back and ask you to make a minor change and you have to dive back in and figure out which files you need to look at. 

Whenver I teach this topic people are surprised I spend so much time on how to organize the setup of your projects or how to name your files. While this all seems like something very simple and common sense, this is where the biggest problems in data science often happen. Let me give you two quick examples. 

The first happened a few years ago. A research group from Duke university analyzed data about human genomes to try to develop a way to predict what chemotherapy each person should get based on their genetic code. They came up with what they thought was a good predictor and published it, then proceeded to start testing it in clinical studies. 

Researchers at MD Anderson got so excited about the result that they tried to find the data and code and do the same analysis as a first step to trying the predictor on their patients. But there was a problem, they couldn't find the data or code. They tried getting it from the researchers at Duke, but it took months of back and forth getting a data set here, a file there, none of it too organized. 

Once they actually managed to get all of the files together and organized, they realized there were some major problems with the predictors that would probably put patients at risk! Ultimately this discovery shut down the clinical studies and led to a major lawsuit. While there were a lot of problems with the original analysis, the reason there was so much trouble was that the files and code weren't organized so it took a _long_ time to figure out the problems that would put patients at risk. 

Another famous example where file organization caused problems was with the scientific paper "Growth in a time of debt". This paper was written by two Harvard economists and suggested that countries with a high level of debt have slow economic growth. 

![Growth in the time of debt scientific paper.](images/02_organizing_projects/02_fileorganization_organizing_projects_02.png)

Unlike most academic papers this paper had a big impact! Many countries used this research to justify austerity measures that impacted social and healthcare programs around the world. 

But it turns out there were some choices the authors made that were questionable or changed their results. This mistake was so important that it was covered by popular shows like The Colbert Show on Comedy Central. The error was actually discovered by a student, but not until much much later. One reason it took so long is the data and analysis files weren't easily available to everyone and organized in a way that the error could be easily identified. 

![The errors in the analysis were discussed on the Colbert Report](images/02_organizing_projects/02_fileorganization_organizing_projects_03.png)


It isn't just because of errors that you'd want to have organized files and projects. Whether its helping your future self, communicating a data science idea, or simply reducing your cognitive load, organizing projects from the start can save you a huge amount of time and hassle.

As Jenny Bryan, one of the most famous data scientists in the world, [says](https://github.com/kbroman/datasciquotes)

> File organization and naming are powerful weapons against chaos.

![Jenny Byran says "File organization and naming are powerful weapons against chaos."](images/02_organizing_projects/02_fileorganization_organizing_projects_04.png)

Another famous data scientist, Karl Broman, [suggests](http://kbroman.org/Tools4RR/assets/lectures/06_org_eda.pdf) that the best way to end up with a good file organization system has three steps.  

* _Step 1_ slow down and make lots of notes for yourself. 
* _Step 2_ have sympathy for your future self. 
* _Step 3_ have a standard system that you understand

A key challenge is that its sometimes hard to feel like file organization is "real work". It isn't coding, or making plots, or writing final documents. Sometimes, when working under a deadline, you will feel pressure to skip file organization in favor of quickly producing results and handing them off. But this never pays off in the long run, the results of poorly organized work almost always fail at some point further down the line. As a general rule of thumb it makes sense to budget 10-20% of the time you will be working on a data science project just to organizing and documenting your work. 

In the rest of this course we will cover one standard system for how to set up, organize, and navigate projects. Once you learn this system you can adapt it to work better for you, or try other ways of organizing your projects. 


### Slides and Video

![Motivation]()

* [Slides]()



{quiz, id: quiz_01_motivation}

? What is the reason file organization caused a problem in the Duke scandal? 

A) It took a long time to discover the problems in the data analysis
b) The disorganized files led to a wrong analysis
c) The files were organized but the researchers wouldn't share them
d) The disorganized files led to people using the wrong data

? What of the following is not a step in Karl Broman's suggestions for project organization?

a) Slow down and make lots of notes for yourself
b) Have sympathy for your future self
c) Have a standard system that you understand
D) Create a set of folders at the beginning of every project


? Which of the following is not a target audience of a data science project?

a) Your coworkers in six months
b) Your coworkers in six months
C) You right now
d) You in six months


{/quiz}
