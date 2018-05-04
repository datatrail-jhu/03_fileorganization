# File naming

This is going to seem like a silly topic to have a whole lecture on. But one of the most frustrating things when looking at someone's data science project is to see a set of files that are completely scattered with names that don't make any sense. It also makes it harder to search for files if they don't have a consistent naming scheme. 

One of the best organized file naming systems is due to [Jenny Bryan]() who gives three key principles of file naming for data science projects. Files should be

* Machine readable
* Human readable
* Be nicely ordered

If your files have these three characteristics, then it will be easy for you to search for them (machine readable), easy for you to understand what is in the files (human readable), and easy for you to glance at a whole folder and understand the organization (be nicely ordered). We'll now discuss some concrete rules that will help you achieve these goals. 


### Machine readable files

The machine we are talking about when we say "machine readable" is a computer. To make a file machine readable means to make it easy for you to use the machine to search for it. Some examples of bad file names are: 

* _analysis.md_ - This file name is too generic and will show up any time you search for "analysis". But you might have hundreds of files like that. 
* _project_final03.md_ - This file name is labeled "final" but then had to be renumbered because the analyst needed to make a change. 
* 



- three principles (jenny bryan)
  - machine readable
  - human readable
  - plays well with default ordering
- machine readble
  - avoid spaces, periods, etc. 
  - use underscores and dashes
  - use lowercase
  - use common "globs" to make it easy to search for files
  - separate globs into "information units"
- human readable
  - name should contain things on content ('slugs')
- default ordering
  - logical use numbers - remember to left pad
  - chronologoiical use dates YYYY-MM-DD
