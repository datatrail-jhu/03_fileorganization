# Setting up data science project folders

Once you have created a new project the next step is to organize and name the folders and files in that project. Naming and organizing files seems very boring, but it one of the most important parts of any data science project! Not having the files or the data available is one of the most common reasons that errors are missed in data science projects. 


### A project organization framework

We will set up data science projects on rstudio.cloud. This is how you should set up every new data science project before you start doing any work. It will be much harder to set up after the project has started and files are scattered everywhere.  Open your web browser and navigate to the website [https://rstudio.cloud/](https://rstudio.cloud/).

![Go to rstudio.cloud](images/02_organizing_projects/02_fileorganization_organizing_projects-4.png)


Then log in and click on the project *my_first_project*.

![Click on my_first_project](images/02_organizing_projects/02_fileorganization_organizing_projects-5.png)



You should now see a screen that looks like this where there are three windows. The window in the lower right hand corner of the screen is the part that shows all the files you have in your project. Right now there shouldn't be any files since we just created this project in the last lesson but didn't do anything in the project. 

![The rstudio.cloud interface showing the empty my_first_project](images/02_organizing_projects/02_fileorganization_organizing_projects-6.png)



Each time you start a new project you will need to create a set of folders for that project. You can create a new folder by clicking on New Folder at the top of the file window. 

![Click New Folder to create a new folder.](images/02_organizing_projects/02_fileorganization_organizing_projects-7.png)


Then you can type in the name of the folder you want to create. First let's create a folder called _data_.

![Name the folder data](images/02_organizing_projects/02_fileorganization_organizing_projects-8.png)


You should now see a folder called data in the file window. 


![We now have a data folder in the files in the project.](images/02_organizing_projects/02_fileorganization_organizing_projects-9.png)

Next we will create a few more folders. For each one click the New Folder button, enter the name and click ok. The folders we need to create will be called *figures*, *code*, and *products*. Once you have created the folders you should see something like this.

![The top level folder structure for every new project](images/02_organizing_projects/02_fileorganization_organizing_projects-10.png)


These folders represent the four parts of any data science project. 

* _data_ - is the folder where you will put all the data you have collected or been given to analyze. 
* _figures_ - is where you will put plots, data pictures, and other images you have created to show data to other people. 
* _code_ - is where you will create code files for collecting, cleaning up, or analyzing data. 
* _products_ - this is the place where you will place any reports, presentations, or products you create for sharing with other people. 

Now that we have these folders in place the next thing you need to create is a README file. This is a file where you will describe all of the data and projects you will be doing. Every project should have a README file so that you can keep notes on what you have done during your project. You will add to this README as your project expands. 

To create the README file click _File_ at the top left hand part of Rstudio. 

![Click on File to create a new file.](images/02_organizing_projects/02_fileorganization_organizing_projects-11.png)

then over over _New File_ to show the types of new files you can create. Move the cursor down and click on _Text File_. 

![Hover over New File and move the cursor to Text File.](images/02_organizing_projects/02_fileorganization_organizing_projects-11.png)


You should see a new screen open with the title _Untitled_ like this. 

![An untitled text file.](images/02_organizing_projects/02_fileorganization_organizing_projects-13.png)



To save the file click on the disk icon in the top left hand corner of the screen. 

![Click on the disk icon to save. ](images/02_organizing_projects/02_fileorganization_organizing_projects-14.png)

Then you can title the file _README.md_ and click _Save_ to save it. 
![Name the file README.md. ](images/02_organizing_projects/02_fileorganization_organizing_projects-15.png)


You should now see the README.md file in your file list on the bottom right of the screen. 

![You have now saved the file README.md. ](images/02_organizing_projects/02_fileorganization_organizing_projects-16.png)


The next thing to do is fill in the README file with the initial description of your project. For now you can copy this text and paste it into your README file, then click the save button.  

`
# This is the README file for my_first_project
The folders in this project are: 

* _data_ - is the folder where you will put all the data you have collected or been given to analyze. 
* _figures_ - is where you will put plots, data pictures, and other images you have created to show data to other people. 
* _code_ - is where you will create code files for collecting, cleaning up, or analyzing data. 
* _products_ - this is the place where you will place any reports, presentations, or products you create for sharing with other people. `

The README file can be used to describe both the high level organization as well as any important special cases about your project. It may be helpful to create additional README files in each subfolder to provide information specific to the files in that subfolder. You would want to link to them from the global README file you have just created. 


### The next level of organization

This is the top level of the organization of a new data science project, but we will usually need to create a little more organization within each folder. For example if you click on the data folder you will see that it is empty. 

![Click on the data folder. ](images/02_organizing_projects/02_fileorganization_organizing_projects-17.png)


You can see at the top of the file organization tab that you are inside the folder *data* which is inside of the folder *project*. 

![Click on the data folder. ](images/02_organizing_projects/02_fileorganization_organizing_projects-18.png)


We need to create two new folders inside of the data folder, one for our raw data and one for our tidy data. You will learn a lot more about them later, but for now use the *New Folder* button

![Click on the New Folder button.. ](images/02_organizing_projects/02_fileorganization_organizing_projects-19.png)


to create one folder called *raw_data* and another called *tidy_data*. 

![Create raw_data and tidy_data folders. ](images/02_organizing_projects/02_fileorganization_organizing_projects-20.png)


One way to write the folders we have now created is like this. 

* data/
  * raw_data/
  * tidy_data/
* code/
* figures/
* products/

Here you can see that the *raw_data* folder is inside of the *data* folder. You can now click on the word *project* at the top of the file window and it will take you back up one level so you will see the folders for data, code, figures, and products. 

![Click on project to view the top level of the directory. ](images/02_organizing_projects/02_fileorganization_organizing_projects-21.png)



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

![A completed project folder. ](images/02_organizing_projects/02_fileorganization_organizing_projects-22.png)


### Slides and Video

![Setting up data science project folders](https://www.youtube.com/watch?v=UbyXBcQgT9A)

* [Slides](https://docs.google.com/presentation/d/1jNeIkKjyVenNF5AEqNpspnLuKXSiXbg-I6VC_uy-b70/edit?usp=sharing)


### Quiz

{quiz, id: quiz_02_organizing_projects}


? What are the top level of folders in a data science project?

A) data, code, figures, and products
b) data, code, figures, and writing
c) data, writing, products, and figures
d) data, figures, writing, and products


? What are the two sub-folders in the data folder?

a) big data, small_data
b) metadata, data
C) raw data, tidy_data
d) data, tidy_data


? When should you set up the project file structure?

a) After you have done your analysis
B) Before starting any new project
c) After you have cleaned the data 
d) When you start to create code files

{/quiz}




