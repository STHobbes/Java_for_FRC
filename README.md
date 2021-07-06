# Java_for_FRC

This is a project with simple coding lessons and examples to help students get up
to speed in using the [WPIlib](https://docs.wpilib.org/en/stable/) Java framework
for FIRST FRC robot programming. The big
obstacle here is the steep initial learning curve because of the very
structured *'everything needs to be a class'* nature of Java, the complexity
of the WPIlib framework, and that running/debugging robot code without a robot or
a robot simulation is a problem. So learning to code on the robot is not a good
recipe for success.

The topics are laid out in jupyter notebooks so students can learn and exercise
the fundamental language concepts of syntax, types, keywords, logic. if-then, loops,
and exception handling; before
worrying about classes, inheritance, interfaces, abstract classes, etc.

##Installing and Using this Project
In order to really use this project, you need to install a lot of stuff. Installation
is quite different for our two primary platforms - windows, and Mac (OSX). I have done
all of the OSX installation in the comfort of my very own home, and have just gone
through the Windows installation with Kai. They are a bit different, so let's document
the details:

###Windows Install/Setup

####Installing `git`
See [1.5 Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) where
there is a section on installing to windows.
####Installing `python`
See [Python Downloads](https://www.python.org/downloads/) which should give you a download
link for the version of windows you are running. At the time I started to put together these
notes the current python version was 3.9.5 - when we installed this on Kai's windows machine,
the `python` command in a console window mapped to the just installed python.
####Installing `jupyter notebooks`
`jupyter notebooks` is written in python and uses python's `pip` installer. Once you have
installed python
####Installing the `IJava` plugin for jupyter notebooks
####Installing `java`
####Installing `jintellij idea` - community edition






###OSX Install/Setup

####Installing `git`
See [1.5 Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) where
there is a section on installing to MacOS. NOTE: I personally do not develop apple apps,
so I have no need or use for xcode. which takes hours to download and install. I go to
[OSX installer from the git website](https://git-scm.com/download/mac) and use the
homebrew installation.
####Installing `python`
See [Python Downloads](https://www.python.org/downloads/) which should give you a download
link for the version of OSX you are running. At the time I started to put together these
notes the current python version was 3.9.5
####Installing `jupyter notebooks`
OSX ships with python 2.7 installed. Even after I install a new python version, if I type
`python` at a console terminal I get something like:
```
roy@ROYs-iMac ~ % python

WARNING: Python 2.7 is not recommended.
This version is included in macOS for compatibility with legacy software.
Future versions of macOS will not include Python 2.7.
Instead, it is recommended that you transition to using 'python3' from within Terminal.

Python 2.7.16 (default, May  8 2021, 11:48:02)
[GCC Apple LLVM 12.0.5 (clang-1205.0.19.59.6) [+internal-os, ptrauth-isa=deploy on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> quit()
roy@ROYs-iMac ~ %
```

To run the just installed python version I use the command `python3` and get:
```
roy@ROYs-iMac ~ % python3
Python 3.9.5 (v3.9.5:0a7dcbdb13, May  3 2021, 13:17:02)
[Clang 6.0 (clang-600.0.57)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> quit()
roy@ROYs-iMac ~ %
```
To install jupyter notebooks into the just installed version of python, in a console
window use the command:
```
pip3 install notebook
```

####Installing the `IJava` plugin for jupyter notebooks
####Installing `java`
####Installing `jintellij idea` - community edition
