---
title:      "Installing & Running Brunnhilde on Windows"
date:       2025-02-10
categories: ['guides']
tags: ['brunnhilde', 'siegfried', 'windows']
---

[Brunnhilde](https://github.com/tw4l/brunnhilde#installation) is a companion tool to [Siegfried]({{< ref "guides/guide-installing-sf-windows" >}}), and Brunnhilde is very useful in creating reports from the inventory and file characterization data that Siegfried creates. While perhaps not essential, it is at this time a highly useful tool that can create reports that are useful for overall analysis of the files you’re working with, as well as a report to keep with the files as useful technical and provenance metadata.

# Installation Step-By-Step

1. Before you install Brunnhilde, you must have Python 3 installed and running. This is likely ready to go if you have completed SI 506. If not, you may need to do that first. Instructions for setting up Python 3 can be found [here](https://docs.python.org/3.9/using/windows.html) and [here](https://code.visualstudio.com/docs/python/python-tutorial). If you prefer to run in a virtual environment, you can also do that. Once Python 3 is ready, proceed to the next step.
2. Open up Visual Studio Code, and open a new Terminal pane there.
3. At the terminal prompt, you can use the pip command to install Brunnhilde: `pip install brunnhilde`.  
_If this doesn't work, you can try running `pip` as a module thus: `$ python -m pip isntall brunnhilde`._
![Installing brunnhilde using python pip install](/images/brunnhilde-pip-install.png "Installing brunnhilde using python pip install")
4. Now, you can call brunnhilde with the command `brunnhilde.py [arguments]` as you would other python programs.  
_Note that you may need to run this as a "module", something like this:_  
`python -m brunnhilde [arguments]`
