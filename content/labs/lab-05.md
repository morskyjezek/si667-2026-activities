---
date: '2026-02-09T17:01:06-05:00'
draft: false
title: 'Lab 05: File Information in the Shell'
categories: ['labs', 'labquestions']
tags: ['files', 'shell']
canvas_link: 'https://umich.instructure.com/courses/812017/assignments/3070587'
---

This lab will allow you to explore concepts and tools related to various digital "materialities" and initial tools to create basic file fixity information, another step toward creating preservation metadata. The files you should use for the assignment are from the course file collection you downloaded previously; if you don't have the files, download an unzip them again from <https://github.com/morskyjezek/si667-2026>.

## Lab Questions: Using the Shell for File Identification and Characterization

### Q1.

Use the `file` command to inspect files and create a MIME Type registry. For this question, use files in the `PKG-text-data` directory.  

a. Create a command to run file with a filter (i.e., the `*`), so that the command outputs file type information for all of the files in the `PKG-text-data/` directory thus printing file characterization information to the terminal display.  

aa. Examine the results. These are all "text files" but they produce different responses when the command runs. Can you identify different text encodings? What else does the output tell you about the files?  

b. Reuse or revise the command you created above to output MIME Types for the files, then output the information to a file called `text-file-types.txt`. Provide the output file.

### Q2.

**Create checksums.** Checksums are algorithmically-generated strings that can be useful to track file fixity. In class, we discussed how to create an [MD5 checksum](https://en.wikipedia.org/wiki/MD5) (a specific algorithm also known as "message digest 5," which produces a 128-bit value, calculated based on the values in a given bitstream, which is unique for that bitstream) for one or more files.  

a. Use the `md5` or `md5sum` command to create checksums for all of the files in the `PKG-text-data/` directory. What command would you use?  

b. Output the list of checksums to a file called `txt-file-checksums.txt`. Provide the output file.

### Q3.

In the previous two steps you created a checksum and listed file types. Do you think this information would be useful to keep as "preservation description information"? Why or why not? What benefit is outputting this information to a file that you might want to keep with the folder if you were going to hang on to it for a while?

## Submitting Your Work

Record your answers in a document file (like txt, doc, rtf, or pdf). Copy and paste questions/problems from above and please maintain numbering. After you've completed your answers to the questions, attach that file to this assignment. Also attach the text files that you created. [Submit responses on Canvas here]({{< pagevar "canvas_link" >}}).

## Key

See the answer key: {{< lab-key-link >}}
