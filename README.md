# QualCoder Debian packages


Debian packages for QualCoder.

Before installing the Debian please install these python packages:

sudo apt install python3-pyqt5 python3-lxml qpdf python3-ebooklib  python3-ply python3-pip

sudo python3 -m pip install pdfminer.six openpyxl

THESE ARE OLDER DEBIANS PLEASE USE THE DEBIANS IN THE RELEASES OF QUALCODER

=====================================================

Use the latest package (qualcoder-2.0.deb). 

Latest package fixes some bugs. Improves the graphical user interface. Adds Japanese language option in the interface. Improved import of special characters (e.g. smart quotes). Imports from Excel xlsx format. Improved visualisation of overlapping codes in text. Improved key short cuts for transcriptions: ctrl P or ctrl S for start/stop play/pause  ctrl R to rewind 5 seconds, alt R rewind 30 seconds, alt F forward 30 secondsctrl D delete speaker names,ctrl N add speaker name ctrl T insert timestamp

These are made using the instructions at: https://help.ubuntu.com/community/PythonRecipes/DebianPackage

And the commands:

fakeroot dpkg --build qualcoder-2.0/ qualcoder-2.0.deb

lintian qualcoder-2.0.deb

## Folder structure:

qualcoder

--DEBIAN

----control

--usr

----bin

------qualcoder   # executable bash with python3 /usr/share/qualcoder/qualcoder.py

----share

------man

--------man1

----------qualcoder.1.gz  # compress with gzip -9

------qualcoder     # python source

------applications

--------qualcoder.desktop

------doc

--------qualcoder

----------changelog.gz   # compress with gzip -9

----------copyright

----------README.md

------pixmaps

--------qualcoder.png
