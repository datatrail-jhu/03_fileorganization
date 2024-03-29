



# Creating and Previewing Markdown Files in RStudio

Because we'll be working a lot in RStudio, it will be useful to learn how to work with Markdown and R Markdown files in RStudio.

We'll start first with creating Markdown files, which will be useful for making short reports or notes that do not contain R code.

### Working with Markdown files

We can create Markdown files in RStudio by going to the File menu and creating a new text file:


![Creating a new file](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g2bfdb07292_0_151)

This opens up a blank file in which you can type your notes in Markdown syntax:


![Adding Markdown text to the blank file](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_1)

When you are finished editing this document and wish to save, you can go to the File menu and select
Save As to save your file:


![Saving the document](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_5)

Enter the name of your file, but be sure to include the file extension .md at the end:


![Entering a new filename](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_9)

When you press Enter, the file will be saved and any Markdown syntax used in your document will show up as color coded:


![The resulting saved file](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_13)

You can continue editing the document and saving with the Save option under the File menu. If you want to create a PDF of this document to share with someone, you can use the Preview functionality shown below:


![Previewing a Markdown document as a PDF](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_17)

If you are prompted to install packages in a dialog box that pops up, click "Yes". After a few seconds a new browser window should pop up containing a preview of the resulting PDF document. If you wish to download this document, you can click the button at the top right:


![Downloading the PDF document](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_21)

Note that when you preview a Markdown file in this way, RStudio will add some header text to the top of your file. You don't need to worry about this or delete this text. It just provides some useful setup information for the next time you use the Preview functionality.

You can also view and download the PDF by clicking the file in the Files pane in RStudio. This will open the PDF in a new tab/window in your web browser.

### Working with R Markdown files

To create an R Markdown document in RStudio, go to the File menu and create a new R Markdown document:


![Creating a new R Markdown document](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_25)

If you are prompted to install packages in a dialog box that pops up, click "Yes" to proceed. You will see the following dialog box appear on your screen. Here you can enter the title of your document as well as your name. For the Default Output Format, we recommend choosing either the HTML or PDF option. After choosing your desired settings, click "OK".


![Setting up options for the R Markdown document](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_43)

Then a new, partially filled-in R Markdown document will open:


![Editing the new R Markdown document](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_47)

You can edit the document by removing the default sections and adding your own notes and code. When you are ready to save, go to the File menu and click "Save As". In the dialog box, you don't need to worry about typing a file extension. RStudio will automatically add the .Rmd extension.


![Saving the R Markdown document](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_51)

In order to convert this document into a PDF document containing your code, plots, and text, you can click the Knit button:


![Knitting the R Markdown document](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/export/png?id=1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0&pageid=g313d64930d_0_58)

**Workflow recommendation:** It is recommended that when you are working with your data with R commands that you type your commands in an R Markdown document instead of below in the Console. In this way, you already begin the process of documenting your steps. You can conveniently send commands from the document to the Console to be run by (1) ensuring that your cursor is on the line of code to be run and (2) hitting Ctrl and Enter simultaneously on the keyboard. You can also select several lines of code to be run and hit Ctrl + Enter.

### Slides and Video

[Automated Videos](https://www.youtube.com/watch?v=XSqdL2XM4xQ)

* [Slides](https://docs.google.com/presentation/d/1BnIEO63i6bo1ZY9HCD9dilG7FgRRzXo1zn1S-c4B8C0/edit?usp=sharing)
