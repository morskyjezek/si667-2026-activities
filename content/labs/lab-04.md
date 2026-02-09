---
date: '2026-02-09T14:15:15-05:00'
draft: false
title: 'Lab 04: Shell Materialities and File Information'
categories: ['labs', 'labquestions']
tags: []
canvas_link: 'https://umich.instructure.com/courses/812017/assignments/3070207'
---

This lab will allow you to explore concepts and tools related that help to understand various digital "materialities" and locate or search within files. The files you should use for the assignment are from the course file collection you downloaded previously; if you don't have the files, download an unzip them again from <https://github.com/morskyjezek/si667-2026>.

## Lab Questions: Using the Shell for Advanced Finding and File Searching

1. **Pipelines.** Create a string of commands that can identify the shortest (by line numbers) TSV file in the `PKG-text-data` directory. Provide the commands you would use. What is the name of the shortest TSV file and how many lines does it have?
2. Using the `find` command (for this question you should be located in the main directory of the course files that you downloaded). What is the `find` command you could use to look (in the current directory and all subdirectories), for all the files?
3. Choose one of the sample datasets for [Assignment 1 (links to Canvas)](https://umich.instructure.com/courses/812017/assignments/2929731). Use these questions to make a preliminary analysis using the sorts of tools and questions we've been asking so far.
  a. What dataset did you choose? What drew you to this dataset?
  b. For this dataset, identify at least one file type that appears to hold data. What is the filetype? How can you find out more about the file type?
  c. Try downloading the file you identified above.
  d. Is it easy or difficult to identify the file, to download the file? Is there any information that you might use to demonstrate provenance or authenticity about the file in the access interface? (For example, how big is the file, a hash value, creator, filename, creation/modification date, etc?)
  e. Using command line tools, can you get detailed technical information about the file? Can you identify the file? Can you get basic information like who created the file and when? If you were able to identify any file information in the previous step from the data interface, does the way that you can interact with or "see" the file in the shell agree with the information you found from the broader context?

***Bonus Question (`find` + `regex`):*** How would you use find with regular expressions to create a list of all image files at the current location (and subdirectories), that is, with extensions `tif`, `tiff`, `jpg`, `jpeg`, `png`, `bmp`, `gif`; then, send that output to a file named `image_file_list.txt`. Put the command and the output list of files in your submission. How would you count how many files you found? How many files did you find?

**HINT 1:** regex will help you with this; you can define an element set using `()` and pipes, like `(x|y)`. BUT, you may need to use pipes and combine with grep.
**Hint 2:** review the [regex slides](https://docs.google.com/presentation/d/1EPhHbuYV3CZ_xYJ9mpk8x3-XmuZ5hLJ_F5wPLteCeDM/edit?usp=drive_link). and the slides on using regex with findLinks to an external site. (see slide 40).

## Submitting Your Work

Submit your work on Canvas. Record your answers in a document file (like `txt`, `doc`, `rtf`, or `pdf`). Copy and paste questions/problems from above and please maintain numbering. After you've completed your answers to the questions, attach that file to this assignment. Also attach the text files that you created.

## Key

See the answer key: {{< lab-key-link >}}
