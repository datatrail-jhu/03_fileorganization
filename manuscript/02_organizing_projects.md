# Organizing projects

Once you have created a new project the next step is to organize and name the folders and files in that project. Naming and organizing files seems very boring, but it one of the most important parts of any data science project! Not having the files or the data available is one of the most common reasons that errors are missed in data science projects. 

One really famous example where file organization caused problems was with the research paper "Growth in a time of debt". This paper was written by two Harvard economists and suggested that countries with a high level of debt experience slow economic growth. Unlike most academic papers this paper had a big impact! Many countries used this research to justify austerity measures that impacted social and healthcare programs around the world. 

But it turns out there were some choices the authors made that were questionable or changed their results. This mistake was so important that it was covered by popular shows like The Colbert Show on Comedy Central. The error was actually discovered by a student, but not until much much later. One reason it took so long is the data and analysis files weren't easily available to everyone and organized in a way that the error could be easily identified. 

It isn't just because of errors that you'd want to have organized files and projects. One of the most common things to happen is that you do a data science project, hand it off to someone else, then move on to a new project. But sometimes people will have questions about your old projects. If you have a system you will be able to find the project and the exact files you need. As Jenny Bryan, one of the most famous data scientists in the world, [says](https://github.com/kbroman/datasciquotes), "File organization and naming are powerful weapons against chaos."

Another famous data scientist, Karl Broman, [suggests](http://kbroman.org/Tools4RR/assets/lectures/06_org_eda.pdf) that the best way to end up with a good file organization system has three steps.  

* _Step 1_ slow down and make lots of notes for yourself. 
* _Step 2_ have sympathy for your future self. 
* _Step 3_ have a standard system that you understand

In the rest of this lesson we will cover one standard system for how to set up the folders you will need to organize a project. Once you learn this system you can adapt it to work better for you, or try other ways of organizing your projects. 

### A project organization framework

We will set up data science projects on rstudio.cloud. Open your web browser and navigate to the website [https://rstudio.cloud/](https://rstudio.cloud/).


Then log in and click on the project my_first_project: 


You should now see a screen that looks like this where there are three windows. The window in the lower right hand corner of the screen is the part that shows all the files you have in your project. Right now there shouldn't be any files since we just created this project in the last lesson but didn't do anything in the project.  

Each time you start a new project you will need to create a set of folders for that project. You can create a new folder by clicking on New Folder at the top of the file window. 

Then you can type in the name of the folder you want to create. First let's create a folder called _data_.

You should now see a folder called data in the file window. 


Next we will create a few more folders. For each one click the New Folder button, enter the name and click ok. The folders we need to create will be called figures, code, and text. Once you have created the folders you should see something like this.

These folders represent the four parts of any data science project. 

* _data_ - is the folder where you will put all the data you have collected or been given to analyze. 
* _figures_ - is where you will put plots, data pictures, and other images you have created to show data to other people. 
* _code_ - is where you will create code files for collecting, cleaning up, or analyzing data. 
* _products_ - this is the place where you will place any reports, presentations, or products you create for sharing with other people. 


Now that we have these folders in place the next thing you need to create is a README file. This is a file where you will describe all of the data and projects you will be doing. You will add to this README as your project expands. 

To create the README file click _File_ at the top left hand part of Rstudio, then over over _New File_ to show the types of new files you can create. Move the cursor down and click on _Text File_. 

You should see a new screen open with the title _Untitled_ like this. 

To save the file click on the disk icon in the top left hand corner of the screen. Then you can title the file _README.md_ and click _Save_ to save it. 

You should now see the README.md file in your file list on the bottom right of the screen. 

The next thing to do is fill in the README file with the initial description of your project. For now you can copy this text and paste it into your README file, then click the save button.  

`
# This is the README file for my_first_project
The folders in this project are: 

* _data_ - is the folder where you will put all the data you have collected or been given to analyze. 
* _figures_ - is where you will put plots, data pictures, and other images you have created to show data to other people. 
* _code_ - is where you will create code files for collecting, cleaning up, or analyzing data. 
* _products_ - this is the place where you will place any reports, presentations, or products you create for sharing with other people. 
`

### The next level of organization

This is the top level of the organization of a new data science project, but we will usually need to create a little more organization within each folder. For example if you click on the data folder you will see that it is empty. 


We need to create two new folders inside of the data folder, one for our raw data and one for our tidy data. You will learn a lot more about them later, but for now use the *New Project* button to create one folder called *raw_data* and another called *tidy_data*. 


One way to write the folders we have now created is like this. 

* data/
  * raw_data/
  * tidy_data/
* code/
* figures/
* products/


Here you can see that the *raw_data* folder is inside of the *data* folder. You can now click on the word *project* at the top of the file window and it will take you back up one level so you will see the folders for data, code, figures, and products. 


The rest of the folders we will need can be written in that same way. The folder structure would look something like this. 

* data/
  * raw_data/
  * tidy_data/
* code/
  * raw_code/
  * final_code/
* figures/
  * exploratory_figures/
  * explanatory_figures/
* products/
  * writing/
  
We need to create the folders *raw_code* and *final_code* inside of the *code* folder. We also need the folders *exploratory_figures* and *explanatory_figures* in the *figures* folder. Finally we need the folder *writing* inside of the *products* folder. 
  
Using the same steps we did for creating the folders inside of the *data* folder, you can create the rest of the folders you will need to organize your data science project. Every time you start a new project you will need to do these steps to set up the folders you will need to store all the files you will be creating. In the next lesson we will talk about how to name the files that will go in these folders. 






