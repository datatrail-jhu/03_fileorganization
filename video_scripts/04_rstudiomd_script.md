Because we'll be working a lot in R Studio, it will be useful to learn how to work with Markdown and R Markdown files in R Studio. We'll start first with creating Markdown files, which will be useful for making short reports or notes that do not contain R code.

We can create Markdown files in R Studio by going to the File menu and creating a new text file.

This opens up a blank file in which you can type your notes in Markdown syntax.

When you are finished editing this document and wish to save, you can go to the File menu and select Save As to save your file.

Enter the name of your file, but be sure to include the file extension dot m d at the end.

When you press Enter, the file will be saved and any Markdown syntax used in your document will show up as color coded.

You can continue editing the document and saving with the Save option under the File menu. If you want to create a PDF of this document to share with someone, you can use the Preview functionality available from the toolbar at the top of the text editor.

If you are prompted to install packages in a dialog box that pops up, click Yes. After a few seconds a new browser window should pop up containing a preview of the resulting PDF document. If you wish to download this document, you can click the button at the top right. Note that when you preview a Markdown file in this way, R Studio will add some header text to the top of your file. You don't need to worry about this or delete this text. It just provides some useful setup information for the next time you use the Preview functionality. You can also view and download the PDF by clicking the file in the Files pane in R Studio. This will open the PDF in a new tab or window in your web browser.

Let's move now to R Markdown files. To create an R Markdown document in R Studio, go to the File menu and create a new R Markdown document.

If you are prompted to install packages in a dialog box that pops up, click Yes to proceed. You will see the following dialog box appear on your screen. Here you can enter the title of your document as well as your name. For the Default Output Format, we recommend choosing either the HTML or PDF option. After choosing your desired settings, click OK.

Then a new, partially filled in R Markdown document will open.

You can edit the document by removing the default sections and adding your own notes and code. When you are ready to save, go to the File menu and click Save As. In the dialog box, you don't need to worry about typing a file extension as we had done for Markdown files. R Studio will automatically add the dot RMD extension.

In order to convert this document into a PDF document containing your code, plots, and text, you can click the Knit button. As a workflow recommendation, it is recommended that when you are working with your data with R commands that you type your commands in an R Markdown document instead of below in the Console. In this way, you already begin the process of documenting your steps. You can conveniently send commands from the document to the Console to be run by first ensuring that your cursor is on the line of code to be run and second hitting control and enter simultaneously on the keyboard. You can also select several lines of code to be run and hit control and enter.