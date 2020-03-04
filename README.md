# QualCoder Debian packages
Debian packages for QualCoder.

Before installing the Debian please install these python packages:

sudo apt install python3-pyqt5 python3-lxml qpdf python3-ebooklib  python3-ply python3-pip

sudo python3 -m pip install pdfminer.six

===

Use the latest package (qualcoder-1.7.deb). 

Earlier packages have reduced functionality and some errors.

These are made using the instructions at: https://help.ubuntu.com/community/PythonRecipes/DebianPackage

And the commands:

fakeroot dpkg --build qualcoder-1.7/ qualcoder-1.7.deb

lintian qualcoder-1.5.deb

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

----------readme

------pixmaps

--------qualcoder.png
