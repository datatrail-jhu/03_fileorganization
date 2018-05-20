# Creating and Previewing Markdown Files in RStudio

Because we'll be working a lot in RStudio, it will be useful to learn how to work with Markdown and RMarkdown files in RStudio.

We'll start first with creating Markdown files, which will be useful for making short reports or notes that do not contain R code.

### Working with Markdown files

We can create Markdown files in RStudio by going to the File menu and creating a new text file:

![Creating a new file](images/04_rstudiomd/04_fileorganization_rstudiomd-1.png)

This opens up a blank file in which you can type your notes in Markdown syntax:

![Adding Markdown text to the blank file](images/04_rstudiomd/04_fileorganization_rstudiomd-2.png)

When you are finished editing this document and wish to save, you can go to the File menu and select
Save As to save your file:

![Saving the document](images/04_rstudiomd/04_fileorganization_rstudiomd-3.png)

Enter the name of your file, but be sure to include the file extension .md at the end:

![Entering a new filename](images/04_rstudiomd/04_fileorganization_rstudiomd-4.png)

When you press Enter, the file will be saved and any Markdown syntax used in your document will show up as color coded:

![The resulting saved file](images/04_rstudiomd/04_fileorganization_rstudiomd-5.png)

You can continue editing the document and saving with the Save option under the File menu. If you want to create a PDF of this document to share with someone, you can use the Preview functionality shown below:

![Previewing a Markdown document as a PDF](images/04_rstudiomd/04_fileorganization_rstudiomd-6.png)

If you are prompted to install packages in a dialog box that pops up, click "Yes". After a few seconds a new browser window should pop up containing a preview of the resulting PDF document. If you wish to download this document, you can click the button at the top right:

![Downloading the PDF document](images/04_rstudiomd/04_fileorganization_rstudiomd-7.png)

Note that when you preview a Markdown file in this way, RStudio will add some header text to the top of your file. You don't need to worry about this or delete this text. It just provides some useful setup information for the next time you use the Preview functionality.

You can also view and download the PDF by clicking the file in the Files pane in RStudio. This will open the PDF in a new tab/window in your web browser.

### Working with RMarkdown files

RMarkdown files will be the main file type you'll be using when working with data. To create an RMarkdown document in RStudio, go to the File menu and create a new RMarkdown document:

![Creating a new RMarkdown document](images/04_rstudiomd/04_fileorganization_rstudiomd-8.png)

If you are prompted to install packages in a dialog box that pops up, click "Yes" to proceed. You will see the following dialog box appear on your screen. Here you can enter the title of your document as well as your name. For the Default Output Format, we recommend choosing either the HTML or PDF option. After choosing your desired settings, click "OK".

![Setting up options for the RMarkdown document](images/04_rstudiomd/04_fileorganization_rstudiomd-9.png)

Then a new, partially filled-in RMarkdown document will open:

![Editing the new RMarkdown document](images/04_rstudiomd/04_fileorganization_rstudiomd-10.png)

You can edit the document by removing the default sections and adding your own notes and code. When you are ready to save, go to the File menu and click "Save As". In the dialog box, you don't need to worry about typing a file extension as we had done for Markdown files. RStudio will automatically add the .Rmd extension.

![Saving the RMarkdown document](images/04_rstudiomd/04_fileorganization_rstudiomd-11.png)

In order to convert this document into a PDF document containing your code, plots, and text, you can click the Knit button:

![Knitting the RMarkdown document](images/04_rstudiomd/04_fileorganization_rstudiomd-12.png)

**Workflow recommendation:** It is recommended that when you are working with your data with R commands that you type your commands in an RMarkdown document instead of below in the Console. In this way, you already begin the process of documenting your steps. You can conveniently send commands from the document to the Console to be run by (1) ensuring that your cursor is on the line of code to be run and (2) hitting Ctrl and Enter simultaneously on the keyboard. You can also select several lines of code to be run and hit Ctrl + Enter.

### Slides and Video

![Markdown in RStudio]()

* [Slides](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/edit?usp=sharing)

{quiz, id: quiz_04_studiomd}

{/quiz}