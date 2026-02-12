---
date: '2026-02-12T15:14:13-05:00'
draft: false
title: 'Lab 07: File Characterization with Siegfried and Brunnhilde'
categories: ['labs', 'labquestions']
tags: ['brunnhilde','siegfried','file characterization']
canvas_link: 'https://umich.instructure.com/courses/812017/assignments/2929740'
---

This week's lab questions are prompts that aim to guide you in the file inspection process and to reflect on the information that you can glean in this process. The problems below are designed to run on the course files, which you have previously downloaded, and that the directory is named `si667-2026-main`.

Note: [this guide page on the course activities site demonstrates using Siegfried and Brunnhilde for file reporting and characterization](guides/guide-running-sf-br/).

## Lab Questions

We will review both of these tools in class, but this lab gives you the chance to explore them first on your own.

**Problem 1:** Create directories to use for the reports, which will be the basis of your PDI.

These tools will generate reports about the files in the directory, so you will first create those directories. Use the `mkdir` command to make two new directories in the course files folder, one titled `sf_out` and the second `br_out`.  

**Problem 2:** Running Siegfried. Siegfried is a useful tool to create an inventory and a bulk process for file characterization information. Run the command on the `PKG-web-files-small` directory and output the reports to the `sf_out` directory.

1.  At the prompt (located in the main file folder, likely called `si667-2026-main` directory), run the command `sf PKG-web-files-small/`. What did the command do? (What files and directory have been created by the command? What do you see in the files?)
2.  At the prompt, enter the following command: `sf PKG-web-files-small/ > sf_out/sf_fileid_report_202602.yaml`. Now what happens?
3.  The previous command should have created some new files in the `sf_out` directory. Open the `sf_out` directory and look around. Answer the following:

*   What did the command do?
*   What does the file tell you?
*   Open the new file in a text editor (e.g., VS Code). How would you characterize the data presented in the file?
*   Does anything strike you as particularly useful? What is odd or questionable about the output?

**Problem 3:** Running Brunnhilde. Brunnhilde produces useful summary reports, as well as the detailed, item-level reports of Siegfried. Your task is to follow the steps demonstrated in the screencast to run brunnhilde.py to analyze the files in the sample file group (instructions on [the slide titled, "Run Brunnhilde"](https://docs.google.com/presentation/d/1gkuf7YhTOoab0q_JRHLZEAc_VTH76LszWAiTKWIBKyo/edit?usp=sharing)). Look at the files that were output when you ran the script, and answer the following:

1.  1.  What did the command do? (What files and directory have been created by the command? What do you see in the files?)
    2.  Focus on the `report.html` file that was created. Take a look at the report (open it in a browser to read it): are there duplicate files, if so, how many? What is the most common image type file (check the MIME Types)? What is the most common application type of file? 
    3.  Are there any duplicate files? If so, what are they named, and how do you think duplicates are identified here?
    4.  In the `report.html` file, look at any of the tables with an "ID" column. What is the information in this column? If you click on any of the links in these columns, where does it take you? What information can you learn at these links? 
    5.  Look at the "unidentified" section of `report.html`. Could you identify any of the files that are listed there? Why do you think the tool was unable to identify these? Now look at the "warnings" section of report.html. How could the information in this section be used to address the questions left in the "unidentified" section?  

[Submit responses on Canvas here]({{< pagevar "canvas_link" >}}).

## Key

See the answer key: {{< lab-key-link >}}
