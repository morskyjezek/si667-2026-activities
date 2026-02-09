---
date: '2026-02-09T14:27:00-05:00'
draft: false
title: 'Lab 04 Key'
categories: ['labs', 'labkey']
tags: []
canvas_link: ''
---

## Question Solutiuons and Commentary for Lab 04

### Q1. 

**Pipelines.** Create a string of commands that can identify the shortest (by line numbers) TSV file in the `PKG-text-data` directory. Provide the commands you would use. What is the name of the shortest TSV file and how many lines does it have?
```bash
$ pwd
~/si667-2026-main/PKG-text-data/

$ wc -l *.tsv | sort -n | head -n 1
```
_In the commands above, the first prompt (running `pwd`) demonstrates that the shell is located in the user's directory corresponding to `PKG-text-data`. The second "pipes" together a series of commands: first, `wc` with the flag `-l` indicating a line count, and using a filter to sort all `.tsv` files (the asterisk); second, the `sort` command sorting by number (`-n`) in descending order; and finally, third, the `head` command to show the beginning of the response with the line number set to show only one line (`-n 1`)._

## Q2.

Using the `find` command (for this question you should be located in the main directory of the course files that you downloaded). What is the `find` command you could use to look (in the current directory and all subdirectories), for all the files?
```bash
$ pwd
~/si667-2026-main/

$ find . -type f
./PKG-legacy-files/01N-0256_emc-000171-01.wps
./PKG-legacy-files/manifest-files.txt
./PKG-legacy-files/a0000003c.gdbtable.sdc
./PKG-legacy-files/ch00001.rtf
./PKG-legacy-files/1898111001_1.txt
./PKG-legacy-files/inventory.docx
./PKG-legacy-files/manifest-details.txt
./PKG-legacy-files/080-b2-tambarani.mp3
./PKG-legacy-files/fertilizeruse.xls
./PKG-text-data/201403160_01_text.json
./PKG-text-data/pg1342.txt
./PKG-text-data/michigan-newspapers.json
./PKG-text-data/2014-01-31_JA-america.tsv
./PKG-text-data/33504-0.txt
./PKG-text-data/pg514.txt
./PKG-text-data/doaj-article-sample.txt
./PKG-text-data/2014-01-31_JA-africa.tsv
./PKG-text-data/2014-02-02_JA-britain.tsv
./PKG-text-data/animals.csv
./PKG-text-data/829-0.txt
./PKG-text-data/tr
./PKG-web-files-small/video/vlwhcssc.asx
./PKG-web-files-small/video/04-04-21full.asf
./PKG-web-files-small/video/glmp_cig.EQ.wm.p20.t12z
./PKG-web-files-small/video/oct17cc.asx
./PKG-web-files-small/pdf/01-1480.pdf
./PKG-web-files-small/pdf/file.pdf
./PKG-web-files-small/pdf/Chapter03.pdf
./PKG-web-files-small/pdf/PFCHEJ.pdf
./PKG-web-files-small/pdf/HR2021 commtext.pdf
./PKG-web-files-small/image/13080t.jpg
./PKG-web-files-small/image/orca.via_.moc_.noaa_.jpg
./PKG-web-files-small/image/k7989-7x.jpg
./PKG-web-files-small/image/m237a2f.gif
./PKG-web-files-small/image/1005107061.tif
./PKG-web-files-small/audio/11-3250JohnsonvFolinoEtAl.wma
./PKG-web-files-small/audio/NEWSLINE_802AF71F439D401585C6FCB02F358307.mp3
./PKG-web-files-small/audio/mj_telework_exchange_final_100710.mp3
./PKG-web-files-small/audio/000727.ram
./PKG-web-files-small/web-files-small-metadata.csv
./PKG-web-files-small/presentation/BudgetandGrants012710.ppt
./PKG-web-files-small/presentation/ADAEMPLOYMENTTaxIncentives.ppt
./PKG-web-files-small/presentation/Non-FTE-Trainee-Activities-060109.ppt
./bit-rot-lab/Wilde_DorianGray.txt
./bit-rot-lab/AY2ghfD.jpg
./bit-rot-lab/ecce-homo.jpg
./bit-rot-lab/tiger_cook_J.jpg
./bit-rot-lab/tiger_cook_T.tiff
./shell/exercise-shell-beyond-basics.md
./shell/exercise-shell-unix-basics.md
./README.md
./samples/simplefile.txt
./samples/pride-prejudice-epub-contents-list.txt
./samples/survey_data_spreadsheet_messy_2022.xlsx
./samples/largepixel-blue.png
./samples/pride-prejudice.epub
./samples/practice-text-regex.txt
./samples/density.tiff
./samples/archive-title.txt
./samples/simplepixel-hexdump
./samples/example-svg.svg
./samples/simplepixel.png
./samples/simplepixel-green.png
./PKG-ndnp/0528.xml
./PKG-ndnp/0528.pdf
./PKG-ndnp/0528.tif
./PKG-ndnp/0528.jp2
./PKG-embedded-metadata/ar99.doc
./PKG-embedded-metadata/The NDSA Levels of Digital Preservation_3.pptx
./PKG-embedded-metadata/pptx-contents-list.txt
./PKG-xml-data/109898358915625.xml
./PKG-xml-data/UF00080115_00001.mets.xml
./PKG-xml-data/example-hathitrust-google-mets.xml
./PKG-what-is-it/empty.file
./PKG-what-is-it/ps.fld/stylesheet.css
./PKG-what-is-it/ps.fld/filelist.xml
./PKG-what-is-it/ps.fld/tabstrip.htm
./PKG-what-is-it/ps.fld/sheet001.htm
./PKG-what-is-it/hi@^9.blob
./PKG-what-is-it/ps.htm
./PKG-what-is-it/ps.xlsx
./PKG-what-is-it/ps.xls
```

_Above, the first prompt confirms the shell's current location. In this case, then top level of the course files. At the second prompt, you will see the `find` command; next, the `.` indicates the current directory/folder; finally, the `-type f` flag indicates all things that the command finds which are files. Additional flags or arguments may be added (see Bonus below) to point the command toward different locations or filter responses differently. After the second prompt, the above block of commands indicates the likely response for the command. Results may differ slightly on your computer, depending on how find handles "hidden" files (those filenames beginning with a dot) or other system files (on MacOS for example, `.DS_Store` is a common file that will appear in directories as a helper for the operating system)._

## Q3.

Choose one of the sample datasets for [Assignment 1 (links to Canvas)](https://umich.instructure.com/courses/812017/assignments/2929731). Use these questions to make a preliminary analysis using the sorts of tools and questions we've been asking so far.
  a. What dataset did you choose? What drew you to this dataset?
  b. For this dataset, identify at least one file type that appears to hold data. What is the filetype? How can you find out more about the file type?
  c. Try downloading the file you identified above.
  d. Is it easy or difficult to identify the file, to download the file? Is there any information that you might use to demonstrate provenance or authenticity about the file in the access interface? (For example, how big is the file, a hash value, creator, filename, creation/modification date, etc?)
  e. Using command line tools, can you get detailed technical information about the file? Can you identify the file? Can you get basic information like who created the file and when? If you were able to identify any file information in the previous step from the data interface, does the way that you can interact with or "see" the file in the shell agree with the information you found from the broader context?

_Answers to the above will vary. Some of the datasets will not provide a single file, some may not provide files of known types, so results will vary._

### Bonus Question

***Bonus Question (`find` + `regex`):*** How would you use find with regular expressions to create a list of all image files at the current location (and subdirectories), that is, with extensions `tif`, `tiff`, `jpg`, `jpeg`, `png`, `bmp`, `gif`; then, send that output to a file named `image_file_list.txt`. Put the command and the output list of files in your submission. How would you count how many files you found? How many files did you find?

**HINT 1:** regex will help you with this; you can define an element set using `()` and pipes, like `(x|y)`. BUT, you may need to use pipes and combine with grep.
**Hint 2:** review the [regex slides](https://docs.google.com/presentation/d/1EPhHbuYV3CZ_xYJ9mpk8x3-XmuZ5hLJ_F5wPLteCeDM/edit?usp=drive_link). and the slides on using regex with findLinks to an external site. (see slide 40).

**Example: Version and response for MacOS running ZSH in Terminal**
```bash
$ pwd
~/si667-2026-main/

$ find -E . -type f -regex '.*\.(tif|tiff|jpg|jpeg|png|bmp|gif)'
./PKG-web-files-small/image/13080t.jpg
./PKG-web-files-small/image/orca.via_.moc_.noaa_.jpg
./PKG-web-files-small/image/k7989-7x.jpg
./PKG-web-files-small/image/m237a2f.gif
./PKG-web-files-small/image/1005107061.tif
./bit-rot-lab/AY2ghfD.jpg
./bit-rot-lab/ecce-homo.jpg
./bit-rot-lab/tiger_cook_J.jpg
./bit-rot-lab/tiger_cook_T.tiff
./samples/largepixel-blue.png
./samples/density.tiff
./samples/simplepixel.png
./samples/simplepixel-green.png
./PKG-ndnp/0528.tif
```

**Example 2: Version and response for Windows running GitBash**
```bash
$ pwd
~/si667-2026-main/

$ find . -type f -regextype posix-extended -regex '.*\.(tif|tiff|jpg|jpeg|png|bmp|gif)'
./PKG-web-files-small/image/13080t.jpg
./PKG-web-files-small/image/orca.via_.moc_.noaa_.jpg
./PKG-web-files-small/image/k7989-7x.jpg
./PKG-web-files-small/image/m237a2f.gif
./PKG-web-files-small/image/1005107061.tif
./bit-rot-lab/AY2ghfD.jpg
./bit-rot-lab/ecce-homo.jpg
./bit-rot-lab/tiger_cook_J.jpg
./bit-rot-lab/tiger_cook_T.tiff
./samples/largepixel-blue.png
./samples/density.tiff
./samples/simplepixel.png
./samples/simplepixel-green.png
./PKG-ndnp/0528.tif
```

_Functionally, the above commands should operate identically. The first prompt confirms the location of the shell. The second prompt runs the `find` command. The main difference betweent the `find` commands is the way in which the regular expressions are referenced: on the MacOS terminal running ZSH (example 1), the `-E` flag indicates "extended" regex, which allows for grouping, then `-regex` introduces the regular expression argument; on the Windows terminal (example 2), the `-regextype` flag and `posix-extended` argument indicate extended regex, and then the `-regex` option introduces the same regular expression. The other elements of the `find` command are the same as above for Q2._

Original lab questions: {{< lab-link >}}
