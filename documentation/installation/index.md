---
layout: docs
currentpage: installation
---

# Installation

- [Installation](#installation)
    - [Hardware Requirements](#hardware-requirements)
    - [Installing Stephanie](#installing-stephanie)
    - [For Non-Programmers](#dummies)
        - [Installing Python3](#install-python)
        - [Install Software](#install-software)
            - [Download Repository](#download-dummy)
            - [install via application](#app-dummy)
            - [install via command line](#cmd-dummy)
    - [For Programmers](#pros)
        - [Check If Python Already Installed](#check_if_installed)
            - [Installing Python 3](#install-python-pro)
        - [Install Software](#install-software-pro)

<hr>

<a name="installation"></a>
## Installation

<hr>

<a name="hardware-requirements"></a>
### Hardware Requirements

The Stephanie has a few minimalistic hardware requirements.
All it basically needs a working computer (PC, laptop, notebook, whatever)
and then these items:

<div class="content-list" markdown="1">
- Windows, Linux or MacOs as operating system.
- Speaker (Basically any audio output device, even headphone would work)
- Mic (Again any audio input device, even bluetooth used for calling would work)
- Internet Connection
</div>

<hr>

<a name="installing-stephanie"></a>
### Installing Stephanie

Stephanie is built on python programming language with
cross-platform support for all the versions of python 3.0 and more.
(Though python 3.5+ is recommended version to use.)

<hr>

<a name="dummies"></a>
#### For Non-Programmers

This part of documentation will guide you through on how to install
Stephanie properly in case you never had any prior knowledge
to programming or coding in general.

<hr>

<a name="install-python"></a>
#### Installing Python3

The very first requirement is having python3 installed in
your local machine, send thanks to awesome developers such that
installing python in any kind of OS is easy as breeze, let's
figure our options of installing python. In case you have python already
installed in your machine, navigate to [check if python already installed](#check_if_installed).

##### Installing via Anaconda (Recommended)

[Anaconda](https://www.continuum.io/downloads){:target="_blank"} is a package-manager and does all of the nasty work
for you to install python in your local machine using good 'ol
.exe setup distribution (just like how you install any game/software)

> A small tip: Don't mess with the settings of the installer just
let it install at C: drive or whatever it chooses according to your OS as well as let it set environment variable just don't mess with it.

To install python3 just go to this link : [https://www.continuum.io/downloads](https://www.continuum.io/downloads){:target="_blank"}
and download the correct installer in accordance to your operating system,
and install python in your local machine. (remember to install python 3.X where X is 4,5,6 and not python 2.7, in short install the most latest version that they are distributing).

##### Via Python.org

Alternatively, you may also install Python from their official website at
[python.org](https://www.python.org/downloads/){:target="_blank"} and just downloading the correct installer
in accordance to your OS and installing it from there (remember to install python 3.X where X is 4,5,6 and not python 2.7).


> A small tip: Don't mess with the settings of the installer just
let it install at C: drive or whatever it chooses according to your OS.

<hr>

<a name="check_if_installed"></a>
###### Checking if python was installed correctly

Once installed, you can check whether everything went correctly or not
by going to start menu and typing cmd in it and the command

    python

which would return you some information about your system and python
, looking somewhat like this indicating python is installed properly:

    Python 3.5.2 |Anaconda custom (32-bit)| (default, Jul  5 2016, 11:45:57) [MSC v.1900 32 bit (Intel)] on win32
    Type "help", "copyright", "credits" or "license" for more information.
    >>>

Make sure it says Python 3.X.Y where X is anything but more than or
equal to 4 and especially not python 2.7! In order to exit, you can press CTRL+Z and then enter.
<hr>

<hr>

<a name="install-software"></a>
#### Installing Software

Once you have python installed in your machine, half of the task is done
leaving the other half which can again be tackled in two ways :

<hr>

<a name="download-dummy"></a>
##### Download (Clone) the github repository

So the first thing you need to do is to download (or as we
call clone by convention) the source code in your machine
through this Github link : [Stephanie-VA](https://www.github.com/slapbot/stephanie-va){:target="_blank"}

This will help you download the repository (repository is
called a folder where all the code is managed.), it will be
in .zip format, so make sure to extract it using winrar, 7zip
or whatever, basic stuff, Now in order to install the software, there are two ways:

<hr>

<a name="app-dummy"></a>
##### Via application

If you don't wanna use command line, 
All you need to do is to get in the extracted folder, there you will find `install.bat` just double click it, that will install everything properly, if needed you can also right click and do open as an administrator, after that
just basically double click `open.bat` and everything will work for you. again you haven't done much of configuration, so not everything will work as expected.
and efficiency won't be good, so let's meet in configuration section, till then you ask basic stuffs from stephanie like,
`"Hey Stephanie, what is the time right now?"`, `"Hey Stephanie, what is the date today?"`, `"Hey Stephanie, you're fired."` and so on.

Now onwards, you can simply use `open.bat` to use stephanie, make a shortcut to that file in desktop if you want.

> **In case you have a linux based system**, then kindly use command line, to run `python install.py` from the extracted folder directory to install all of the modules effectively. While in order to run the application, you can use `python index.py`. Basically batch file is written with windows in mind, since working with command line is kind of a norm as far as linux systems are concerned. In case you have any trouble, you can always restort to via command-line listed below, or ask a query at one of the links listed below of the page to get help.

<hr>

<a name="cmd-dummy"></a>
##### Via command-line (cmd, powershell, git bash, terminal, etc)

I probably recommend doing this way unless you just don't have interest in programming or you just don't have time or you are sure you will fuck it up, because it will give you
a slight exposure around how command line works and if it fails, you can always root back to application way to install, so command line is the most
basic utility for any programmer, and let's not forget how "hackerish" it
looks too. You just need to learn few commands and you're good to go.

- Go to start-menu and type cmd, and right click on `cmd.exe`, it will open a pop up menu, click run as administrator so you have all the permissions.

- now you can go to the folder, where you extracted the repository, (downloaded files) and open that folder.
Now just copy the location where this folder is present, basically how 'url' works in chrome, if you click on it, that will show the path of that folder. For example :
In windows 7 your address bar will have something like this :
( // means a comment, just don't, argh, forget that thing, don't copy it or something)

        > computer > Local Disk(D:) > softwares > stephanie // clicking on this will get
        D:\softwares\stephanie // copy this text

- Now get back to your command line, and type cd "your copied address", what it does
is that it changes the directory where cmd opens by default to location, where stephanie is located.
Make sure cd is lowercase and after that there's a space and copied address is present inside
quotation marks ("____") where ____ = copied address, like so:

        cd "J-U-S-T P-A-S-T-E W-H-A-T Y-O-U C-O-P-I-E-D B-E-F-O-R-E"

- So awesome, now you're in the correct folder, and everything is going good. Now all
you need to do is type this command `python install.py` Okay so some new
command, Eh? Again it's simple as mouse, that command basically says run `install.py` which is the module written to install all of the dependencies needed to run stephanie. It gets all the code made from different people and install it
in your machine for you to use. `requirements.txt` denote to a file present in stephanie, which I added, has
the information about all the code I needed to make stephanie. Cool? Cool.

        python install.py

- And with that all the dependencies are in place, everything is ready to go, see just a couple of commands
and you are on your road to become a badass tony stark.
Finally, you can actually test stephanie, though you haven't configured it yet, but if you type commnd `python index.py`,
Stephanie will start working. Gon try it, type command:

        python index.py

This command will result in saying : `Stephanie is on.` meaning everything worked.
Now by default speech to text engine is set to google speech,
with wake-up engine set to False. more information will be provided in configuration section.
All it means is that stephanie is ready to work, but it doesn't has all the functionality, and wouldn't work the best yet.

You can do basic stuffs like ask, `Hey Stephanie, what is the time right now?`
after having fun, close stephanie, by using keyboard shortcut, `CTRL + C` repeatedly or giving command, `Stephanie, you're fired.`
or just closing the command line altogether, whenever you wanna use stephanie, you can write the command, `python index.py` from the directory in which stephanie lies to invoke the application.

<hr>

<a name="pros"></a>
#### For Programmers

This part of documentation will guide you through on how to install
Stephanie properly in case you have some knowledge to programming or coding in general. If know yo know basic commands
and stuffs, this is for you.

<hr>

<a name="install-python-pro"></a>
#### INSTALLING PYTHON3

So hopefully, you have python 3.4 or more installed in your computer, if not, no problem there mate, installing it is easy as pie,
especially with package managers like anaconda or just do it from official source, though I'd still recommend anaconda, check this
[install python](#install-python)

<hr>

<a name="install-software-pro"></a>
#### INSTALLING STEPHANIE

Once you have python3 installed in your computer you can install stephanie quite easily.

- Just Clone/Downlaod this repository [Stephanie-VA](www.github.com/slapbot/stephanie-va){:target="_blank"} in your machine, extract it, and open command prompt as administrator in that folder.

- Install all the dependencies through the command :

        pip install -r requirements.txt

    Or by simply executing the `install.py` script, or just clicking `install.bat` which is a wrapper around `install.py`.

- And run the application using command :

        python index.py

- Alternatively instead of running command python index.py, you can also simple execute `open.bat`, but former one works best
if you have some kind of command line preference, for instance I frickin love cmder.

- To close the application, simple close the command line, or press CTRL + C, you can also say `"Hey Stephanie, you're fired"` to close it.

- Since you haven't done any configuration, stephanie won't work at it's best, will have limited functionality and efficiency won't be
the best either, try commands like `"Hey Stephanie, what is the time right now?"` or `"Hey stephanie, what is the date today?"` to test it and Let's meet
in the [configurations section](/documentation/configuration)
