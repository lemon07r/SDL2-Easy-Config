Quick Setup with CLion (For Windows 64 bit with MinGW)
OPTIONAL: I recommend having these folders in an easy to find place, like a folder in documents called SDL.

CMakeListsTemplate
Use the template from CMakeListsTemplate as a guideline for your CMakeLists.txt file.

CMakeScripts
The CMakeScripts folder should be copied to the root of your project directory, this includes all the needed FindSDL2*.cmake scripts.

DevLibs
The DevLibs folder contains all the needed development libraries, be sure to set the path variables to the directories in this folder in your CMakeLists.txt file.

Runtimes
The DLLs from the Runtimes folder are needed to run the compiled binaries (included ones are for Windows 64 bit).
These can be saved to your C:\Windows\System32\ folder if you want to be able to run the binaries without having the DLLs in the same directory if you are on Windows.

