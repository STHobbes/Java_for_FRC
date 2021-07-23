# Java_for_FRC
status: in development
version: 0.0.1 alpha

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

# Installing and Using this Project
In order to really use this project, you need to install a lot of stuff. Installation
is quite different for our two primary platforms - windows, and Mac (OSX). I have done
all of the OSX installation in the comfort of my very own home, and have just gone
through the Windows installation with Kai and on the driver station laptop. They are a
bit different, so let's document the details:

## Installing `java`
Go to the latest 
[Java SE Development Kit 16 Downloads](https://www.oracle.com/java/technologies/javase-jdk16-downloads.html):

### Windows Install/Setup
Download the
[Windows x64 Installer](https://www.oracle.com/java/technologies/javase-jdk16-downloads.html#license-lightbox).
Double-click on the downloaded installer in your Downloads folder to install.

### OSX Install/Setup
Download the
[macOS Installer](https://www.oracle.com/java/technologies/javase-jdk16-downloads.html#license-lightbox).
Double-click on the downloaded installer in your Downloads folder to install.
### Finishing Up, Windows or OSX
Verify you have the correct Java installed. Close and reopen your console terminal (to make sure it
has the most recent changes to the environment) and type the command `java --version`. You should
get something like this:

<blockquote><pre><code>
C:\Users\frc> <b>java --version</b>
java 16.0.1 2021-04-20
Java(TM) SE Runtime Environment (build 16.0.1+9-24)
Java HotSpot(TM) 64-Bit Server VM (build 16.0.1+9-24, mixed mode, sharing)
</code></pre></blockquote>

## Installing `python`
See [Python Downloads](https://www.python.org/downloads/) which should give you a download
link for the version of windows or OSX you are running. At the time I started to put together these
notes the current python version was 3.9.5 (what we installed this on Kai's windows machine).

Double-clock on the downloaded installer to install `python`.

### Windows Install/Setup
If you run python in a console or command window you should be able to type `python` and
see something like:
<blockquote><pre><code>
C:\Users\frc> <b>python</b>
Python 3.9.6 (tags/v3.9.6:0a7dcbdb13, May  3 2021, 13:17:02) [MSC v.1929 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
</code></pre></blockquote>

Type `quit()` at the `>>>` prompt to end python. What you are looking for here is that the version number
matches the version you just installed.

### OSX Install/Setup
OSX ships with python 2.7 installed. Even after I install a new python version, if I type
`python` at a console terminal I get something like:
<blockquote><pre><code>
roy@ROYs-iMac ~ % <b>python</b>

WARNING: Python 2.7 is not recommended.
This version is included in macOS for compatibility with legacy software.
Future versions of macOS will not include Python 2.7.<br>
Instead, it is recommended that you transition to using 'python3' from within Terminal.

Python 2.7.16 (default, May  8 2021, 11:48:02)
[GCC Apple LLVM 12.0.5 (clang-1205.0.19.59.6) [+internal-os, ptrauth-isa=deploy on darwin
Type "help", "copyright", "credits" or "license" for more information.
&gt;&gt;&gt; <b>quit()</b>
roy@ROYs-iMac ~ %
</code></pre></blockquote>

To run the just installed python version I use the command `python3` and get:

<blockquote><pre><code>
roy@ROYs-iMac ~ % <b>python3</b>
Python 3.9.5 (v3.9.5:0a7dcbdb13, May  3 2021, 13:17:02)
[Clang 6.0 (clang-600.0.57)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
&gt;&gt;&gt; <b>quit()</b>
roy@ROYs-iMac ~ %
</code></pre></blockquote>

## Installing `jupyter notebooks`
`jupyter notebooks` is written in python and uses python's `pip` installer. This installer finds,
downloads, and installs the latest version of a python package.

### Windows Install/Setup
In a console window use the command:

<blockquote><pre><code>
C:\Users\frc> <b>pip install notebook</b>
</code></pre></blockquote>

You will see a lot of progress bars scroll by as notebook installs.

### OSX Install/Setup
To install jupyter notebooks into the just installed version of python, we use
the `pip` installer, and similarly to running the latest version of python,
we append a `3`in the console command to get the right version of `pip` to match
the installed python. To install `noteboolk`::

<blockquote><pre><code>
roy@ROYs-iMac ~ % <b>pip3 install notebook</b>
</code></pre></blockquote>

You will see a lot of progress bars scroll by as notebook installs.

### Installing the `IJava` plugin for jupyter notebooks
`jupyter notebooks` was originally written for python. We need to install a plugin for Java development. The
plugin is an open source github project [SpencerPark/IJava](https://github.com/SpencerPark/IJava). The
latest release is [version 1.3.0](https://github.com/SpencerPark/IJava/releases/tag/v1.3.0), and at the bottom
of that page is the download link for
[ijava-1.3.0.zip](https://github.com/SpencerPark/IJava/releases/download/v1.3.0/ijava-1.3.0.zip) which
you want to download.

### Windows Install/Setup
In your files explorer, go to your Download folder and right-click on the downloaded
`ijava-1.3.0.zip` and select **`expand all`** to unzip the file. After the file is expended (unzipped), you
should see an `ijava-1.3.0` folder in your `Downloads` folder. Assuming you are in your user folder
with your command prompt (the command window opens to your user window by default) These are the
commands you would use to install `ijava`

<blockquote><pre><code>
C:\Users\frc> <b>cd Downloads\ijava-1.3.0</b>
C:\Users\frc\Downloads\ijava-1.3.0> <b>python install.py</b>
C:\Users\frc\Downloads\ijava-1.3.0\install.py:164: DeprecationWarning: replace is
 ignored. Installing a kernelspec always replaces an existing installation
 install_dest = KernelSpecManager().install_kernel_spec(
Installed java kernel into "C:\ProgramData\jupyter\kernels\java"
C:\Users\frc\Downloads\ijava-1.3.0> <b>cd ..\..</b>
C:\Users\frc>
</code></pre></blockquote>

### OSX Install/Setup
In your finder, go to your Download folder and double-click on the downloaded
`ijava-1.3.0.zip` unzip the file. After the file unzipped, you
should see an `ijava-1.3.0` folder in your `Downloads` folder. Assuming you are in your user folder
with your command prompt (the command window opens to your user window by default) These are the
commands you would use to install `ijava`

<blockquote><pre><code>
roy@ROYs-iMac ~ % <b>cd Downloads/ijava-1.3.0</b>
roy@ROYs-iMac ijava-1.3.0 % <b>python3 install.py</b>
install.py:164: DeprecationWarning: replace is ignored. Installing a kernelspec always replaces an existing installation
install_dest = KernelSpecManager().install_kernel_spec(
Installed java kernel into "/usr/local/share/jupyter/kernels/java"
roy@ROYs-iMac ijava-1.3.0 % <b>cd ../..</b>
roy@ROYs-iMac ~ %
</code></pre></blockquote>

We have seen cases where there is a permissions error writing to `/usr/local/share/jupyter` which
normally means the permissions on  the `/usr/local/share` directory don't allow you to
write into that directory unless you are running as an admin user. In that case, try using

<blockquote><pre><code>
roy@ROYs-iMac ijava-1.3.0 % <b>sudo python3 install.py</b>
</code></pre></blockquote>

which will run the command as the superuser. You will need the admin password to do that, however, if
this is your computer, you should have admin privileges, and the password will just be your normal password.

## Running your own notebook for learning Java

I recommend you create a directory (folder) for your exercises in learning Java. Below I created a
`learningJava` directory, changed directory to `learningJava`, and started the notebook in that
directory. When you do this you will get a bunch printed out, and a new tab will open in you browser
displaying your notebook:

### Running notebook in windows

<blockquote><pre><code>
C:\Users\frc> <b>mkdir learningJava</b>
C:\Users\frc> <b>cd learningJava</b>
C:\Users\frc\learningJava> <b>python -m notebook</b>
</code></pre></blockquote>

### Running notebook in OSX

<blockquote><pre><code>
roy@ROYs-iMac ~ % <b>mkdir learningJava</b>
roy@ROYs-iMac ~ % <b>cd learningJava</b>
roy@ROYs-iMac learningJava % <b>python3 -m notebook</b>
</code></pre></blockquote>

## Installing `git`, and running this project's notebook

### Windows Install/Setup
See [1.5 Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
where there is a section on installing to windows. It notes the windows download is at
[https://git-scm.com/download/win](https://git-scm.com/download/win).

### OSX Install/Setup
See [1.5 Getting Started - Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
where there is a section on installing to MacOS. NOTE: I personally do not develop apple apps,
so I have no need of, or use for xcode, which takes hours to download and install. I go to
[OSX installer from the git website](https://git-scm.com/download/mac) and use the
homebrew installation notes:

### Installing ***jintellij idea*** - community edition



on OSX, remember to set preferences.


