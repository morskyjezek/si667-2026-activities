---
date: '2026-02-21T11:25:36-05:00'
draft: false
title: 'Lab 07 Key'
categories: ['labs', 'labkey']
tags: ['brunnhilde','siegfried','file characterization']
canvas_link: ''
---

## Lab Guidance and Solutions

**Problem 1:** Create directories to use for the reports, which will be the basis of your PDI.

_Use the `mkdir` command to make two new directories in the course files folder, one titled `sf_out` and the second `br_out`._

**Problem 2:** Running Siegfried. Siegfried is a useful tool to create an inventory and a bulk process for file characterization information. Run the command on the `PKG-web-files-small` directory and output the reports to the `sf_out` directory.

1.  At the prompt (located in the main file folder/directory, likely called `si667-2026-main`), run the command `sf PKG-web-files-small/`. What did the command do? (What files and directory have been created by the command? What do you see in the files?)  
_This command runs the Siegfried tool and initiates a Siegfried file identification report for the `PKG-web-files-small` directory, scanning each file contained in the directory. The tool generates a report on each file, which is formatted in a plain-text style called [YAML](https://en.wikipedia.org/wiki/YAML), and prints this report out to the terminal display. The first few lines of the output should look something like this:_  
```
---
siegfried   : 1.11.4
scandate    : 2026-02-20T16:12:45-05:00
signature   : default.sig
created     : 2026-01-23T17:32:13+11:00
identifiers :
  - name    : 'pronom'
    details : 'DROID_SignatureFile_V122.xml; container-signature-20260119.xml'
---
filename : 'PKG-legacy-files/01N-0256_emc-000171-01.wps'
filesize : 18451
modified : 2026-01-13T21:00:40-05:00
errors   : 'mscfb: directory entries error finding sector (mscfb: FAT index is $
matches  :
  - ns      : 'pronom'
    id      : 'fmt/111'
    format  : 'OLE2 Compound Document Format'
    version :
    mime    :
    class   : 'Text (Structured)'
    basis   : 'byte match at 0, 30'
    warning :
---
filename : 'PKG-legacy-files/080-b2-tambarani.mp3'
filesize : 12705156   
modified : 2026-01-13T21:00:40-05:00
errors   :
matches  :   
  - ns      : 'pronom'
    id      : 'fmt/134'
    format  : 'MPEG 1/2 Audio Layer 3'
    version :
    mime    : 'audio/mpeg'
    class   : 'Audio'
    basis   : 'extension match mp3; byte match at 0, 7559 (signature 5/9)'
    warning :
---
filename : 'PKG-legacy-files/1898111001_1.txt'
filesize : 70200
modified : 2026-01-13T21:00:40-05:00
errors   :
matches  :
  - ns      : 'pronom'
    id      : 'fmt/101'
    format  : 'Extensible Markup Language'
    version : '1.0'
    mime    : 'application/xml'
    class   : 'Text (Mark-up)'
    basis   : 'byte match at 0, 19'
    basis   : 'byte match at 0, 19'
    warning : 'extension mismatch'  
---
```
2. At the prompt, enter the following command: `sf PKG-web-files-small/ > sf_out/sf_fileid_report_202602.yaml`. Now what happens?  
_This command repeats the previous step, but it adds an output so that instead of the report appearing in the display, it will be saved in the file named `sf_fileid_report_202602.yaml` in the `sf_out` folder/directory._
3. The previous command should have created a new file in the `sf_out` directory. Open the `sf_out` directory and look around. Answer the following:  
  * What did the command do?
  * What does the file tell you?
  * Open the new file in a text editor (e.g., VS Code). How would you characterize the data presented in the file?
  * Does anything strike you as particularly useful? What is odd or questionable about the output?  
  _There are multiple answers to this question, but some things to note include that the file is in YAML markup, it contains information about the Siegfried tool version that was used, it contains an entry about each file in the corresponding directory, and the report has file characterization information as well as information about how that information was determined (using a file extension or a format identification signature or 'magic number')._

**Problem 3:** Running Brunnhilde. Brunnhilde produces useful summary reports, as well as the detailed, item-level reports of Siegfried. Your task is to follow the steps demonstrated in the screencast to run `brunnhilde.py` to analyze the files in the same folder as the previous step (i.e., the `PKG-web-files-small` folder; see general instructions on [the slide titled, "Run Brunnhilde"](https://docs.google.com/presentation/d/1gkuf7YhTOoab0q_JRHLZEAc_VTH76LszWAiTKWIBKyo/edit?usp=sharing)). Look at the files that were output when you ran the script, and answer the following:

1.  1.  What did the command do? (What files and directory have been created by the command? What do you see in the files?)  
_The command runs the brunnhilde tool and creates additional file characterization information and preservation metadata._
    2.  Focus on the `report.html` file that was created. Take a look at the report (open it in a browser to read it): are there duplicate files, if so, how many? What is the most common image type file (check the MIME Types)? What is the most common application type of file?  
    _Brunnhilde did not identify any duplicate files in this directory. The most common image type is JPEG, there are three files identified as JPEGs. As far as applications, brunnhilde identifies five files of PDF types. Note that these answers, which are based on the outputs of the MIME type, differ from the information in the "File formats" section, where you can see the five PDF files, but they are separated into different versions of PDF; the most frequent versions are 1.3 and 1.4, which each show two samples._
    3.  Are there any duplicate files? If so, what are they named, and how do you think duplicates are identified here?  
    _The web files directory does not appear to have any duplicate files. If it did, however, brunnhilde would use checksums to identify identical bitstreams._
    4.  In the `report.html` file, look at any of the tables with an "ID" column. What is the information in this column? If you click on any of the links in these columns, where does it take you? What information can you learn at these links?  
    _You will find an "ID" column in the "File formats" and "File format versions" tables. These identifiers link back to the PRONOM file registry database, which provides additional information about the technical requirements and characteristics of that file type._
    5.  Look at the "unidentified" sections of `report.html`. Could you identify any of the files that are listed there? Why do you think the tool was unable to identify these? Now look at the "warnings" section of report.html. How could the information in this section be used to address the questions left in the "unidentified" section?  
    _There are two files in the "unidentified" section, `000727.ram` and `oct17cc.asx`, they are in folders titled `audio` and `video` respectively. As far as "warnings," this section has information about five files; the most common mistakes appear to be related to files that are only identified based on the file extension or where the extension does not appear to match the file content. While the report does claim the file types in the "Unidentified" section are "unknown," note that the "Warning" column does have information that suggests a possible PRONOM match for each, and that could merit further investigation._

## Lab Questions

Lab questions page: {{< lab-link >}}
