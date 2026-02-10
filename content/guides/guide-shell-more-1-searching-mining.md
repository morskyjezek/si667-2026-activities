---
title: 'Shell 2: Searching and Data Mining'
draft: true
categories: ['guides']
tags: ['shell','bash','find','grep']
---

_This guide is generally adapted to working in a UNIX environment using the bash shell, but there are various nods to Mac and Windows, which have some differences. Demonstrations during class assume use of Mac OS/Unix style terminal commands. However, commands for both unix and windows environments are offered below. See the linked resources at the bottom for greater detail._

## Finding files

Beyond looking at a file's contents, or "inspecting," you will often need to find files
at any point in the operating system or a storage device.

The `find` command is a useful way to find files. The syntax is somewhat more complicated than
other commands, but it can be a powerful way to get an overview of items in a particular drive or directory.
One of the things tha makes `find` useful is that you can give it very detailed instructions about where to
look and what to look for. The syntax for `find` is as follows:

* `find` + `{location you want to search}` + `{options that you want to search for, designated by hyphen flags, like -type or -name of object, followed by the arguments for each`

For example:

* `find . -type f -name '*.txt'`

In the above:
* `find` initiates the find program,
* `.` indicates to search the current directory (you could specify
a different path here); note that in this case, the command is _recursive_, which means that
it will search any directories contained in the current path (`.`), but that is another thing you can
control if you investigate the options for this program further,
* `-type f` defines what type of object to look for, in this case `f` designates files
(you can also use `d` for directories or find other options here using the `man` page)
* `-name '*.txt'` limits the results to anything that has a string ending with the text `.txt`
in the name of the object.

Find can also be adapted to search for patterns using regular expressions. For example:

* `find -E . -type f -regex ".*\.tiff?"`

In the above, the option `-E` indicates that the regular expression will use advanced operators
(in this case, the question mark).
Then it is similar to the above, it looks for objects that are files.
Finally, `-regex` indicates regular expression, followed by the expression in double quotes.
In this example, the expression looks for matches that are strings with any number of any characters (`.*`),
have a dot (`\.`), have a string of tif (`tif`), and then have zero or one instances of the 
character f (`f?`). In plain language, this expression will look in the current directory, 
search all of the files, and return matches for files ending with `.tif` or `.tiff`, which
are both likely possible extensions for a tif file.



This guide is intended to offer additional information about the `find` `grep` command.
That section, however, remains under development, so for the time being,
please consult the related [command reference slide deck](https://docs.google.com/presentation/d/1OZyh3pcNeZ2NIyGptQuR_idpbW9SbMe0ZLuAtsr8Q14/edit?usp=sharing).