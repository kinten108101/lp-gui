# Linux Print Graphical User Interface.

# Prerequisite
Remember to update your system:
    sudo apt update
Install YAD, where I build the GUI:
    sudo apt install yad
Install pdfinfo:
    sudo apt install pdfinfo

# Installation
Clone this repo anywhere:
    git clone https://github.com/kinten108101/lp-gui.git
Simply run lp-gui
    cd lp-gui; ./lp-gui

For convenience, you'd like to execute lp-gui from anywhere. There are many ways to achieve this.

You could copy lp-gui to home/[username]/bin. With this, start by:
    lp-gui
Another way would be to add the directory that contains lp-gui to PATH.
Open home/[username]/.profile (create one if it does not exist). Add this line to the end of the file:
    PATH="[enter the directorys path here]:$PATH"
Relogin.
Samewise, start by:
    lp-gui
For those who don't know how this works, check out [environmental variables](https://help.ubuntu.com/community/EnvironmentVariables).

# Compatibility
Tested on Ubuntu 20.04, should work on most distros that use bash.
Windows will be considered, althought there should be no need for pdf readers there are already well-equipped with these features.

# TBA
- Recreate this in NodeJS

