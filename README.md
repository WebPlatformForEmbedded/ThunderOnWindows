# ThunderOnWindows
Artifacts required to build Thunder on a windows platform

This reository holds the binaries and header files, required to build the Thunder framework on windows. Furthermore it ontains information on how to setup a VisualStudio2019 build on windows.

# Evironment setup
The default solution is setup in such away that it can run and load the Thunder and Thunder Nano Services (capable of running in Windows) if both repositories are next to each other. So checkout Thunder on disk and put the ThunderNanoServices next to it.

e.g. C:\Users\Me\Thunder C:\Users\Me\ThunderNanoServices

Sources: https://github.com/RDKCentral/Thunder and https://github.com/RDKCentral/ThunderNanoServices

Install this repository in:
git clone https://github.com/WebPlatformForEmbedded/ThunderOnWindows C:\Users\Me\Thunder\Source

Depending on the filesystem used by the windows OS, symbolic links are supported or not. There is 1 Symbolic link in the Thuder repository (Thunder/Source/tools -> "../Tools"). If this symbolic link does not exist, you will experience build errors (error 2, GenrateProxyStub.py not found). or create a copy of the Tools directory in Source/tools (xcopy /d ..\Tools tools) or create the symlink manually (mklink /D tools "..\Tools")

Make sure you have python:
https://www.python.org/downloads/release/python-382/

and the jsonref:
pip install jsonref


# Running Thunder on windows
For the Thunder UI to be serviced on windows, you need to manually copy the repository contents:
https://github.com/rdkcentral/ThunderUI/tree/master/dist
to
<DATAPATH>/Controller/UI

