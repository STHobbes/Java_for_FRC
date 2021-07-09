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

## Installing and Using this Project
In order to really use this project, you need to install a lot of stuff. Installation
is quite different for our two primary platforms - windows, and Mac (OSX). I have done
all of the OSX installation in the comfort of my very own home, and have just gone
through the Windows installation with Kai and on the driver station laptop. They are a
bit different, so let's document the details:

### Windows Install/Setup

#### Installing `java`
Go to the latest 
[Java SE Development Kit 16 Downloads](https://www.oracle.com/java/technologies/javase-jdk16-downloads.html)
and download the
[Windows x64 Installer](https://www.oracle.com/java/technologies/javase-jdk16-downloads.html#license-lightbox).
Double-click on the downloaded installer in you Downloads folder to install.

Veryfy you have the correct Java installed. Close and reopen your console terminal (to make sure it
has the most recent changes to the environment) and type the command `java --version`. You should
get something like this:
```
C:\Users\frc> java --version 
java 16.0.1 2021-04-20
Java(TM) SE Runtime Environment (build 16.0.1+9-24)
Java HotSpot(TM) 64-Bit Server VM (build 16.0.1+9-24, mixed mode, sharing)
```

#### Installing `python`
See [Python Downloads](https://www.python.org/downloads/) which should give you a download
link for the version of windows you are running. At the time I started to put together these
notes the current python version was 3.9.5 (what we installed this on Kai's windows machine)

if you run python in a console or command window you should be able to type `python` and
see something like:
```
C:\Users\frc> python
Python 3.9.6 (tags/v3.9.6:0a7dcbdb13, May  3 2021, 13:17:02) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

Type `quit()` at the `>>>` prompt to end python. What you are looking for here is that the version number
matches the version you just installed.

#### Installing `jupyter notebooks`
`jupyter notebooks` is written in python and uses python's `pip` installer. Once you have python installed
use the command.
```
C:\Users\frc> pip install notebook
```
You will see a lot of progress bars scroll by as notebook installs.

#### Installing the `IJava` plugin for jupyter notebooks
`jupyter notebooks` was originally written for python. We need to install a plugin for Java development. The
plugin is an open source github project [SpencerPark/IJava](https://github.com/SpencerPark/IJava). The
latest release is [version 1.3.0](https://github.com/SpencerPark/IJava/releases/tag/v1.3.0), and at the bottom
of that page is the download link for
[ijava-1.3.0.zip](https://github.com/SpencerPark/IJava/releases/download/v1.3.0/ijava-1.3.0.zip) which
you want to download. In your files explorer, go to your Download folder and right-click on the downloaded
`ijava-1.3.0.zip` and select **`expand all`** to unzip the file. After the file is expended (unzipped), you
should see an `ijava-1.3.0` folder in your `Downloads` folder. Assuming you are in your user folder
with your command prompt (the command window opens to your user window by default) These are the
commands you would use to install `ijava`

`C:\Users\frc>`**` cd Downloads\iJava-1.3.0`**  
`C:\Users\frc\Downloads\iJava-1.3.0>`**` python install.py`**  
`C:\Users\frc\Downloads\iJava-1.3.0\install.py:164: DeprecationWarning: replace is`  
` ignored. Installing a kernelspec always replaces an existing installation`  
` install_dest = KernelSpecManager().install_kernel_spec(`  
`Installed java kernel into "C:\ProgramData\jupyter\kernels\java"`  
`C:\Users\frc\Downloads\iJava-1.3.0>`**` cd ..\..`**  
`C:\Users\frc>`  

#### Running your own notebook for learning

I recommend you create a directory (folder) for your exercises in learning Java. Below I created a
`learningJava` directory, changed directory to `learningJava`, and started the notebook in that
directory. When you do this you will get a bunch printed out, and a new tab will open in you browser
displaying your notebook:

<code>
C:\Users\frc> <b>mkdir learningJava</b>  
C:\Users\frc> <b>cd learningJava</b>  
C:\Users\frc> <b>python -m notebook</b>  
</code>



#### Installing `git`, and running this project's notebook
See [1.5 Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) where
there is a section on installing to windows. It notes the windows download is at
[https://git-scm.com/download/win](https://git-scm.com/download/win).

#### Installing `jintellij idea` - community edition






### OSX Install/Setup

#### Installing `git`
See [1.5 Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) where
there is a section on installing to MacOS. NOTE: I personally do not develop apple apps,
so I have no need or use for xcode. which takes hours to download and install. I go to
[OSX installer from the git website](https://git-scm.com/download/mac) and use the
homebrew installation.
#### Installing `python`
See [Python Downloads](https://www.python.org/downloads/) which should give you a download
link for the version of OSX you are running. At the time I started to put together these
notes the current python version was 3.9.5
#### Installing `jupyter notebooks`
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

#### Installing the `IJava` plugin for jupyter notebooks
#### Installing `java`
#### Installing `jintellij idea` - community edition
