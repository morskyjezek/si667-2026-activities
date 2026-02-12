---
date: '2026-02-12T12:47:18-05:00'
draft: false
title: 'Lab 05 Key'
categories: ['labs', 'labkey']
tags: ['fixity','checksums','file','md5','integrity']
canvas_link: 'https://umich.instructure.com/courses/812017/assignments/3070587'
---

This lab will allow you to explore concepts and tools related to various digital "materialities" and initial tools to create basic file fixity information, another step toward creating preservation metadata. The files you should use for the assignment are from the course file collection you downloaded previously; if you don't have the files, download an unzip them again from <https://github.com/morskyjezek/si667-2026>.

## Lab Questions: Using the Shell for File Identification and Characterization

### Q1.

Use the `file` command to inspect files and create a MIME Type registry. For this question, use files in the `PKG-text-data` directory.  

a. Create a command to run file with a filter (i.e., the `*`), so that the command outputs file type information for all of the files in the `PKG-text-data/` directory thus printing file characterization information to the terminal display.  

```bash
$ file PKG-text-data/*

PKG-text-data/2014-01-31_JA-africa.tsv:  ASCII text, with very long lines (413)
PKG-text-data/2014-01-31_JA-america.tsv: ASCII text, with very long lines (406)
PKG-text-data/2014-02-02_JA-britain.tsv: ASCII text, with very long lines (396)
PKG-text-data/201403160_01_text.json:    JSON data
PKG-text-data/33504-0.txt:               Unicode text, UTF-8 (with BOM) text
PKG-text-data/829-0.txt:                 Unicode text, UTF-8 text
PKG-text-data/animals.csv:               CSV text
PKG-text-data/doaj-article-sample.txt:   CSV text
PKG-text-data/michigan-newspapers.json:  JSON data
PKG-text-data/pg1342.txt:                Unicode text, UTF-8 (with BOM) text
PKG-text-data/pg514.txt:                 Unicode text, UTF-8 (with BOM) text
```

aa. Examine the results. These are all "text files" but they produce different responses when the command runs. Can you identify different text encodings? What else does the output tell you about the files?  

_The list indicates that some are in ASCII text or Unicode, and some are listed as UTF-8, a specific type of UniCode. These are indications of the text encoding. Overall, this tells us that while these are similar in content (that is, they are all meant at some level to be "text"), they differ in format (that is, they have different elements of structure, such as text encoding and file type)._

b. Reuse or revise the command you created above to output MIME Types for the files, then output the information to a file called `text-file-types.txt`. Provide the output file.

```bash
$ file -I PKG-text-data/*.*

PKG-text-data/2014-01-31_JA-africa.tsv:  text/plain; charset=us-ascii
PKG-text-data/2014-01-31_JA-america.tsv: text/plain; charset=us-ascii
PKG-text-data/2014-02-02_JA-britain.tsv: text/plain; charset=us-ascii
PKG-text-data/201403160_01_text.json:    application/json; charset=us-ascii
PKG-text-data/33504-0.txt:               text/plain; charset=utf-8
PKG-text-data/829-0.txt:                 text/plain; charset=utf-8
PKG-text-data/animals.csv:               text/csv; charset=us-ascii
PKG-text-data/doaj-article-sample.txt:   text/csv; charset=utf-8
PKG-text-data/michigan-newspapers.json:  application/json; charset=us-ascii
PKG-text-data/pg1342.txt:                text/plain; charset=utf-8
PKG-text-data/pg514.txt:                 text/plain; charset=utf-8
```

**Nota bene:** The above command will be slightly different on Mac & Windows. If you are running windows, the command would be `file -i PKG-text-data/*`.

### Q2.

**Create checksums.** Checksums are algorithmically-generated strings that can be useful to track file fixity. In class, we discussed how to create an [MD5 checksum](https://en.wikipedia.org/wiki/MD5) (a specific algorithm also known as "message digest 5," which produces a 128-bit value, calculated based on the values in a given bitstream, which is unique for that bitstream) for one or more files.  

a. Use the `md5` or `md5sum` command to create checksums for all of the files in the `PKG-text-data/` directory. What command would you use?  

```bash
$ md5 -r PKG-text-data/*

7bf627c61206e593714fb43b49997261 PKG-text-data/2014-01-31_JA-africa.tsv
c77ed0104498a43fc8dc86667825c156 PKG-text-data/2014-01-31_JA-america.tsv
a83e9a6514b01567b2cf861d6a00acea PKG-text-data/2014-02-02_JA-britain.tsv
4f00f6738afd560519a6cf41756228cc PKG-text-data/201403160_01_text.json
8dbc442349ab803233675ceba13f5a95 PKG-text-data/33504-0.txt
cf3f6ce27978e65233025af7f876ffdb PKG-text-data/829-0.txt
c2ed3b02105dd0081eac853bdf2edf9f PKG-text-data/animals.csv
a5b232b358327777a8f3c448f0bee605 PKG-text-data/doaj-article-sample.txt
c2bbcf459264b6018bac8f146e2e39bb PKG-text-data/michigan-newspapers.json
a689b4d90e2ab6a580365100008a5037 PKG-text-data/pg1342.txt
586511c9a49eb98e54b189b1dd4822ab PKG-text-data/pg514.txt
d41d8cd98f00b204e9800998ecf8427e PKG-text-data/tr
```

**Nota bene:** The command to create an MD5 checksum on Windows is `md5sum`. The command to produce output similar to the above would be: `md5sum PKG-text-data/*`.

b. Output the list of checksums to a file called `txt-file-checksums.txt`. Provide the output file.

```bash
$ md5 -r PKG-text-data/* > txt-file-checksums.txt
```

### Q3.

In the previous two steps you created a checksum and listed file types. Do you think this information would be useful to keep as "preservation description information"? Why or why not? What benefit is outputting this information to a file that you might want to keep with the folder if you were going to hang on to it for a while?

_Answers here will vary. However, it is important to mention that the above commands produce at least two critical pieces of the OAIS-defined Preservation Description Information (PDI): fixity information, which is provided by the MD5 checksum (note that MD5 is not the only option, there are other algorithms that can be used to create a checksum); and context information, which is the file name and designator within the file system._

Original lab questions: {{< lab-link >}}
