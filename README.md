# QualCoder Debian packages

Now JULY 2020 - soon due for another release as a few changes have occured.

Debian packages for QualCoder.

Before installing the Debian please install these python packages:

sudo apt install python3-pyqt5 python3-lxml qpdf python3-ebooklib  python3-ply python3-pip

sudo python3 -m pip install pdfminer.six openpyxl

=====================================================

Use the latest package (qualcoder-1.9.deb). 

Earlier packages have reduced functionality and some errors.

These are made using the instructions at: https://help.ubuntu.com/community/PythonRecipes/DebianPackage

And the commands:

fakeroot dpkg --build qualcoder-1.9/ qualcoder-1.9.deb

lintian qualcoder-1.9.deb

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
