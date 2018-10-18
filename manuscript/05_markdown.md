# Introduction to Markdown

We learned briefly about Markdown and RMarkdown documents in the previous lesson. Markdown is a basic markup language designed to be displayed on the web.  With a few basic commands, you can create polished documents that can be used to:

* Communicate your results to others
* Provide daily/weekly reports of your employer

### How to use Markdown

If you know how to type you know how to use Markdown! Writing with Markdown is the exact same task as writing in a text editor like Microsoft Word. The only difference is that all the fancy buttons and options are removed and instead replaced with a series of commands that you can type to format your text.

### Markdown Example

Here's a small example of what Markdown can do! You can see everything in this document is written as plain text, with just letters and basic symbols.

![An example markdown file](images/05_markdown/05_fileorganization_markdown-1.png)

Now you can see how that text appears when it is rendered in Markdown.  Even though it was created with plain text, it appears with italics, bolding, different sized text, and even an image!

![A rendered markdown file](images/05_markdown/05_fileorganization_markdown-2.png)

### Main commands

Three major formatting basics of Markdown are headers, bold and italicized text, and lists. Headers help you separate sections of your document, bold or italicized format allows you to emphasize important points in your document, and lists help you orderly arrange your ideas.

#### Headers

Headers are straightforward. To create a header, you simply add a # sign right before the text you want to make a header. Keep in mind the # must be on the beginning of a new line (no text on the line before it). The more #'s you add before the text, the smaller the header will be. For example here is a list of headers you can use ordered from largest to smallest.

```r
# Largest
## Slightly less large
### Even less large
#### Even smaller
##### Smaller still
###### Smallest shown here (but you can go smaller!)
```

The reason why this did not register as a header is because it is formatted it as a comment. By inserting three tick marks before and after the block of text you wish to comment, it will not execute any formatting. Without the tick marks here is what we get! 

![A rendered markdown file](images/05_markdown/05_fileorganization_markdown-3.png)

The headers look as we wanted them too.  Thus headers should *not* be included in code chunks. If pound signs (#) are within a code chunk, Markdown will consider them to be comments, rather than headers.

#### Bolded and italicized text

Creating bolded and italicized text is also very straightforward.  Use a double asterisk (`**`) before and after the text you want to be bold and a single asterisk (`*`) before and after text you want to italicize.

```r
So in this sentence **what you want to bold** is shown **bolded** and *what you want to italicize* is shown in *italics*.
```

See the results here:

So in this sentence `**what you want to bold**` will be shown **what you want to bold** and `*what you want to italicize*` will be shown *what you want to italicize*.

#### Lists

Lists are a useful way to organize your ideas or tasks.  In Markdown, you can make your lists numbered or non-numbered.  To make a numbered list, just put the number and a period in front of the item.  As with headers, you do need to make sure your first number is on a new line (no text on the line before it!)

```r
1. First item
2. Second item
3. Third item
```
This becomes:

1. First item
2. Second item
3. Third item

For non-numbered lists, you can use your choice of asterisks (`*`), pluses (`+`), or minuses (`-`) to indicate list items:

```r
* First item
* Second item
```

 OR
 
 ```r
+ First item
+ Second item
```

OR

```r
- First item
- Second item
```

All become:

+ First item
+ Second item


You can create sub-items for your list by indenting (using multiple spaces or Tab) before the number or the asterisk/plus/minus.  Make the number or symbol of the sub-item line up with the text of the item above it!

```r
1. First item
2. Second item
   1. Sub-item
   2. Sub-item
3. Third item
   * Sub-item
   * Sub-item
```

This becomes:

1. First item
2. Second item
   1. Sub-item
   2. Sub-item
3. Third item
   * Sub-item
   * Sub-item

If you want to cross off items on your list (as you do them, perhaps) you can create a strike-through using double tildas (`~~`).

```r
1. ~~First item~~
2. Second item
   1. ~~Sub-item~~
   2. Sub-item
```

This becomes:

1. ~~First item~~
2. Second item
   1. ~~Sub-item~~
   2. Sub-item

### More complicated editing

There are many more text modifiers you can use for Markdown. A short instructional guide can be found [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

You will see some more of these commands later in this module, but you might want to bookmark the above link now for future reference!

### Links

Links to content on the internet can be included in a Markdown document as well.  The format for a link is to put what you want your link to say in square brackets followed immediately by the web address where the link should go inside of parentheses, like this: 

```r
[What you want your link to say](Web address where the link should go)
```

For example if you want the link to go to www.google.com when clicked, then you'd replace the text in the parentheses and write:

```r
[What you want your link to say](www.google.com)
```
This is what it would look like in your rendered Markdown file: 

[What you want your link to say](www.google.com)

If you want to change the text of the link itself, you just change what's in the square brackets. For example, you might want the sentence: If you don't know the answer, you should look it up on Google, where the word Google would be a link to www.google.com.  You could do that by putting Google into square brackets, with the web address www.google.com following immediately in parentheses, like this:

```r
If you don't know the answer, you should look it up on [Google](www.google.com).
```
This would be shown as:

If you don't know the answer, you should look it up on [Google](www.google.com).

You can insert images in a Markdown document as well. This is done in a similar manner to links. For images you can add `![Image Caption](/path_to_image/image_name.png)`. The link can be the web location of an image or the local address of an image.

For instance, if you type `![Yosemite National Park](https://commons.wikimedia.org/wiki/Yosemite_National_Park#/media/File:Half_Dome_from_Glacier_Point,_Yosemite_NP_-_Diliff.jpg)` will show this.

![Yosemite National Park](images/05_markdown/05_fileorganization_markdown-12.png)



### Slides and Video

![Introduction to Markdown](https://www.youtube.com/watch?v=0mc0DfoqN5A)

* [Slides](https://docs.google.com/presentation/d/1eHhYKegVodplOm9MajA3OaWReEMo7YRER-IRWBivWJM/edit?usp=sharing)


{quiz, id: quiz_05_markdown}

### Introduction to Markdown quiz

{choose-answers: 4}
?1 How would you produce bolded text like **some text**? 

C) `**some text**`
C) `__some text__`
o) `*some text*`
o) `_some text_`
o) `~~some text~~`
o) `--some text--`
o) `~some text~`
o) `* some text`
o) `_bold_some text_\bold`

{choose-answers:4}
?1 How would you produce italicized text like *some text*? 

C) `*some text*`
C) `_some text_`
o) `**some text**`
o) `__some text__`
o) `~~some text~~`
o) `--some text--`
o) `~some text~`
o) `* some text`
o) `_bold_some text_\bold`

{choose-answers: 4}
?2 Which of the following would give you the smallest header (an H4 header)? 

C) `#### My header`
o) `## My header`
o) `### My header`
o) `# My header`
o) `_H4_My header_\H4`
o) `#H4 My header`
o) `####H4 My header`

{choose-answers: 4}
?2 Which of the following would give you the largest header (an H1 header)? 

C) `# My header`
o) `#### My header`
o) `## My header`
o) `### My header`
o) `_H4_My header_\H4`
o) `#H4 My header`
o) `####H4 My header`

{choose-answers: 4}
?3 Which of the following is a correctly formatted hyperlink?

C) `[Google](www.google.com)`
m) `![Google](www.google.com)`
o) `###www.google.com`
o) `*www.google.com*`
o) `**www.google.com**`
o) `_www.google.com`
o) `__www.google.com__`

{choose-answers: 4}
?3 Which of the following demonstrates how you would include the image `image.png` in your Markdown document?

C) `![Google](image.png)`
m) `[Google](image.png)`
o) `###image.png`
o) `*image.png*`
o) `**image.png**`
o) `_image.png_`
o) `__image.png__`

{/quiz}
