# What is Markdown?

Objectives:
- Learn what markdown is and what it is used for
- Learn the major markdown script modifiers
- Realize anyone who can type can use markdown!

## What is Markdown? 

Markdown is a basic markup language designed to be displayed on the web.  With a few basic commands, you can create polished documents that can be used to:

* Communicate your results to others
* Provide daily/weekly reports of your employer

## How do you use Markdown?

If you know how to type you know how to use Markdown! Writing with Markdown is the exact same task as writing in a text editor like Microsoft Word. The only difference is that all the fancy buttons and options are removed and instead replaced with a series of commands that you can type to format your text.

## Markdown Example

Here's a small example of what Markdown can do!

What you type:

![An example markdown file](images/02_whatismarkdown/03_fileorganization_whatismarkdown-1.png)

How it appears:

![A rendered markdown file](images/02_whatismarkdown/04_fileorganization_whatismarkdown-2.png)

## Main commands

Three major formatting basics of Markdown are headers, bold and italicized text, and lists. Headers help you separate sections of your document, bold or italicized format allows you to emphasize important points in your document, and lists help you orderly arrange your ideas.

### Headers

Headers are straightforward, you simply add a # sign right before the text you want to make a header. Keep in mind the # must be on the beginning of a new line (no text on the line before it). The more #'s you add before the text, the smaller the header will be. For example here are a list of headers you can use ordered from largest to smallest.

```
# Largest
## Slightly less large
### Even less large
#### Even smaller
##### Smaller still
###### Smallest shown here (but you can go smaller!)
```

The reason why this did not register as a header is because it is formatted it as a comment. By inserting three tick marks before and after the block of text you wish to comment, it will not execute any formatting. Without the quotation marks here is what we get!

# Largest
## Slightly less large
### Even less large
#### Even smaller
##### Smaller still
###### Smallest shown here (but you can go smaller!)

### Bolded and italicized text

Creating bolded and italicized text is also very straightforward.  Use a double asterisk (`**`) before and after the text you want to be bold and a single asterisk (`*`) before and after text you want to italicize.

```
So in this sentence **what you want to bold** is shown **bolded** and *what you want to italicize* is shown in *italics*.
```

See the results here:

So in this sentence **what you want to bold** is shown **bolded** and *what you want to italicize* is shown in *italics*.

### Lists

Lists are a useful way to organize your ideas or tasks.  In Markdown, you can make your lists numbered or non-numbered.  To make a numbered list, just put the number and a period in front of the item.  As with headers, you do need to make sure your first number is on a new line (no text on the line before it!)

```
1. First item
2. Second item
3. Third item
```
This becomes:

1. First item
2. Second item
3. Third item

For non-numbered lists, you can use your choice of asterisks (`*`), pluses (`+`), or minuses (`-`) to indicate list items:

```
* First item
* Second item
```
 OR
 
 ```
+ First item
+ Second item
```

OR
```
- First item
- Second item
```

All become:

* First item
* Second item


You can create sub-items for your list by indenting (using multiple spaces) before the number or the asterisk/plus/minus.  Make the number or symbol of the sub-item line up with the text of the item above it!

```
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

```
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

There are many more text modifiers you can use for Markdown. A long form instructional guide can be found [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) while a shorter straight to the point version can be found [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

You will see some more of these commands later in this module, but you might want to bookmark the above links now for future reference!
