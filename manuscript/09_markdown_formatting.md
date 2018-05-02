# Formatting in R Markdown

To get you started, we'll practice some of the formatting that is inherent to R Markdown documents. 

To start, let's look at bolding and italicizing text. To bold text, you surround it by two asterisks on either side. Similarly, to italicize text, you surround the word with a single asterisk on either side. `**bold**` and `*italics*` respectively. 

We've also seen from the default document that you can make section headers. To do this, you put a series of hashtags/octothorpes/pound signs/whatever you want to call this (#) mark. The number of hash marks determines what level of heading it is. One hash is the highest level and will make the largest text (see the first line of this lecture), two hashes is the next highest level and so on. Play around with this formatting and make a series of headers, like so:

# Header level 1
## Header level 2
### Header level 3... 

The other thing we've seen so far is code chunks. To make an R code chunk, you can type the three backticks, followed by the curly brackets surrounding a lower case R, put your code on a new line and end the chunk with three more backticks. Thankfully, RStudio recognized you'd be doing this a lot and there are short cuts, namely Ctrl+Alt+I (Windows) or Cmd + Option + I (Mac). Additionally, along the top of the source quadrant, there is the "Insert" button, that will also produce an empty code chunk. Try making an empty code chunk. Inside it, type the code `print("Hello world")`. When you knit your document, you will see this code chunk and the (admittedly simplistic) output of that chunk. 

If you aren't ready to knit your document yet, but want to see the output of your code, select the line of code you want to run and use Ctrl+Enter or hit the "Run" button along the top of your source window. The text "Hello world" should be output in your console window. If you have multiple lines of code in a chunk and you want to run them all in one go, you can run the entire chunk by using Ctrl+Shift+Enter OR hitting the green arrow button the right side of the chunk OR going to the Run menu and selecting Run current chunk. 

One final thing we will go into detail on is making bulleted lists, like the one at the top of this lesson. Lists are easily created by preceding each prospective bullet point by a single dash, followed by a space. Importantly, at the end of each bullet's line, end with TWO spaces. This is a quirk of R Markdown that will cause spacing problems if not included.  

- Try  
- Making 
- Your  
- Own  
- Bullet  
- List!

This is a great starting point and there is so much more you can do with R Markdown. Thankfully, RStudio developers have produced an ["R Markdown cheatsheet"](http://www.rstudio.com/wp-content/uploads/2016/03/rmarkdown-cheatsheet-2.0.pdf) that we urge you to go check out and see everything you can do with R Markdown! The sky is the limit! 

### Summary

In this lesson we've delved into R Markdown, starting with what it is and why you might want to use it. We hopefully got you started with R Markdown, first by installing it, and then by generating and knitting our first R Markdown document. We then looked at some of the various formatting options available to you and practiced generating code and running it within the R Studio interface. 

### Slides and Video

This lesson's slides can be found [here](https://docs.google.com/presentation/d/1vMEbcs-jih32ORJpQduKjDx9cMxjJs9TBjXiUGXwpY8/edit?usp=sharing)  
The lesson's video can be found [here]()  

### Quiz

{quiz, id: quiz15}  
? How would you strike through some text?  

A) `~~strikethrough~~`   
b) `--strikethrough--`  
c) `\strikethrough\`  
d) None of the above 
 
{/quiz}}
