# LP-GUI, Linux-based duplex printing with GUI

## Description

A user-friendly printing GUI which port essential printing features from those on Windows to Linux. CUPS (Common UNIX Printing System) is mostly available on Linux distros but are terminal-based and unintuitive to navigate through. This is an unofficial extension for CUPS and also doubles as a testing ground for experimental features.

## Feature

- Emulated duplex (double-sided) printing for otherwise unsupported printers (tested on Epson L3110)
- Support for printing strategies from [josephj11's duplex utility script](https://sourceforge.net/projects/duplexpr/)\*
- Fixed page range
- Formulaic page range\*
- Short binding edge\*
- Other essentials: Number of copies, multiple pages per sheet\*, color, page size (A4, Letter, Legal).

Unfortunately other brand-exclusive features/utilies can't be ported, contact their websites for further assistance if possible.

*(\*)TBA*

## Prerequisite

Remember to update your system:

    $ sudo apt update

Install YAD, where I build the GUI:

    $ sudo apt install yad

Install pdfinfo:

    $ sudo apt install pdfinfo

## Installation

Clone this repo anywhere:

    $ git clone https://github.com/kinten108101/lp-gui.git

Simply run `lp-gui`:

    $ cd lp-gui; ./lp-gui

A config file (`home/[username]/.profile-lp-gui`) will be created on your first run. These settings will be loaded on running lp-gui, so you may take some time reconfiguring it to your system's preference.

## Advanced

For convenience, you'd like to execute lp-gui from anywhere. There are many ways to achieve this.

You could copy lp-gui to `home/[username]/bin`, a directory that should be included in `PATH`. After this, start by simply:

    $ lp-gui

If you are against moving the file around, perhaps add this repo's folder to `PATH` directly.
Open `home/[username]/.profile` (create one if it does not exist). Add this line to the end of the file:

    $ x="[path to repo's clone]"
    $ if [ -d $x ]; then
    $ PATH="$x:$PATH";
    $ fi

`.profile` will be run on your next login. After that, start by:

    $ lp-gui

For those who don't know how this works, check out [environmental variables](https://help.ubuntu.com/community/EnvironmentVariables).

## How does it work?

*Basic math + YAD for GUI + some week's worth of work because i'm a noob = profit!*

## Compatibility

Tested on Ubuntu 20.04, should work on most distros that use bash.
Windows will be considered, although there should be no need as there are already well-equipped pdf-readers (Adobe Acrobat, Foxit Reader) with these features.

## TBA

- Keep on debugging.
- Migrate this to JS, so expect delays in new features.

