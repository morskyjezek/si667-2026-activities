---
title:      "Running Siegfried & Brunnhilde"
categories: ['guides']
tags: ['brunnhilde', 'siegfried']
---

This page contains the instructions for running tools that can help with file reporting. These are useful tools that can create some of the preservation description information, which might accompany an information package, and to create technical information that can be used for tracking file integrity and duplication.

# Setup

The following sections show how to get set up to run the file reporting tools.

## Sample Files

All of the activities will use the course's sample files, which you should have previously downloaded during class in January. If you didn't download them, have lost those files, or want a new copy, they are located in the course github repository, and you can download them all directly as a zip file at [{{< githubRepo >}}]({{< githubRepo >}}). Unzip that folder somewhere on your computer, for example in your `Desktop` or `Documents` folder. This should result in a folder named `si667-2026-main`, which will match the demonstrations below. (_Nota bene: the screencasts below were recorded in 2023 and 2024, so some of the sections in the videos may show those years in its name, but assume any paths or other references should be to 2026._)

# Install Siegfried

To install Siegfried, follow the instructions at the tool's site: [https://www.itforarchivists.com/siegfried/#install](https://www.itforarchivists.com/siegfried/#install). These instructions work well if you're using a Unix-style system (such as a Linux machine or Mac OS). The instructions use another tool, HomeBrew, which is a useful utility to manage command line programs, and if you need that, see the program's homepage for good installation instructions (note that it will require an internet connection): [https://brew.sh/](https://brew.sh/).

If you're running on a different style of system, like Windows, the instructions are a bit less specific. If you have had trouble following those instructions, [try these step-by-step instructions for Windows]({{< ref "guides/guide-installing-sf-windows" >}}). Linux systems may require more modifications.

# Install Brunnhilde

Brunnhilde is a python-based tool, so you can install it as you would other Python extensions using `pip`. The process is explained on the tool's site: [https://github.com/tw4l/brunnhilde#installation](https://github.com/tw4l/brunnhilde#installation).

If those instructions aren't working well, here is a [Windows-specific walkthrough of the installation process]({{< ref "guides/guide-running-brunnhilde-windows" >}}).

# Check if the tools are running

This screencast shows how to see if the tools are running:

{{< youtube z1GOoispJ5k >}}

# Running `brunnhilde.py`

This screencast explains how `brunnhilde.py` works and demonstrates how to run the command:

{{< youtube yuZQmpnjKhE >}}
