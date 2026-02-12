+++
date = '2026-02-08T15:26:08-05:00'
draft = false
title = 'Lab 02 Key'
canvas_link = ''
categories = ['labs', 'labkey']
tags = ['labkey']
+++

For reference, see the [shell slide deck](https://docs.google.com/presentation/d/1OZyh3pcNeZ2NIyGptQuR_idpbW9SbMe0ZLuAtsr8Q14/edit?usp=drive_link) and [this reference document in the course GitHub repo](https://github.com/morskyjezek/si667-2026/blob/main/shell/exercise-shell-unix-basics.md).

## Questions to Answer

**Q1.** Imagine that you have opened a window that gives access to the command line. What command would you use to determine your current location (current path)?

```bash
$ pwd
```

**Q2.** What command would you use to move to another directory or folder?

```bash
$ cd
```

**Q3.** What command would you use to list the contents of the directory or folder?

```bash
$ ls
```

**Q4.** You can request a basic list (names of files and directories) and an advanced, or "long" list (that shows permissions, file size, path, etc), by adding the option `-l`. What command and options would you use to generate the basic list for the folder named `shell`? What commands and options generate the advanced list?

```bash
$ ls -l shell/
```

**Q5.** Problem: During class, you downloaded and unzipped some course files (see [Wk 2 slide no. 60](https://docs.google.com/presentation/d/1a_6SjtFxCYt9OwSjh7yvYOP1e14J6BiOkrrIVGoHR_E/edit?usp=sharing)). If you didn't complete that activity, download the files, unzip them, and keep track of where the files are located. In a command shell window, navigate to the location of those files. Once you are there, print a list of the files in that location. Compare the list of files you see with the list of files listed in the [course GitHub repository](https://github.com/morskyjezek/si667-2026). Can you identify the same files in both locations?

_You should see an identical list of files. In some cases, there may be minor differences, such as the presence of added system files, like `.DS_Store` in MacOS. But these differences should be minor._

**Q6.** Using the full list of files you printed with the "long" list to the command line (in Q4), modify that command so that it would save your list into a file called `files-list.txt`. What is the command?

```bash
$ ls -l shell/ > files-list.txt
```

**Q7.** What have you learned about using the command line? Are there situations or tasks where you imagine this environment to be more (or less) useful than the graphical interface of the Explorer or Finder?

_There are many possible things you might observe, including:  
- precision (more specific and repeatable than the graphical interface),  
- portability (easier to share a written command than in graphical interface),  
- ability to recreate actions in different operating systems,  
- repeatability (quickly recreate or repeat actions based on basic patterns, e.g., list all of the text files in a location),  
- use filters and patterns (that is, using "globbing" or characters like `*` to match multiple characters, it is possible to find results based on given criteria, not just ranges or individual items)._

Original lab questions: {{< lab-link >}}.
