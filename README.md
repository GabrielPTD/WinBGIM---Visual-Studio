# What is WinBGIM?
WinBGIm is a Windows C++ graphics library based on the classic Borland Graphics Interface (originally distributed with Borland’s Turbo Pascal and later with their Turbo C compilers). In addition to the original BGI interface, WinBGIm also provides programmer support for accessing the mouse and for using the graphics window as a C++ ostream.

# How to build?
This repository provides precompiled library compatible with **Visual Studio 2017**, to use it on other Visual Studio versions you will have to recompile the library.
* Open the solution `LibBGI.sln` with Visual Studio, select the desired configuration `Release` or `Debug` and then simply Build the solution.
* In the main folder (where `LibBGI.sln` is located) will be created a folder named after the choosed configuration(`Release` or `Debug`), inside you will find the lib `LibBGI.lib`.
* Replace the old lib (`LibBGI.lib`) from the folder `precompiled` with the one you just compiled.
  
  
# How to install?
* Create a new Visual Studio Project or open an existing one.
* In `Solution Explorer` right click on the project, select `Properties`:
  * Go to `VC++ Directories`:
    * In tab `Include Directories` add the path to `precompiled/include` (it can be found in this repository).
    * In tab `Library Directories` add the path to `precompiled/library` (it can be found in this repository).
  * Go to `Linker` -> `Input` and in tab `Additional Dependencies` insert this `LibBGI.lib`.
* Done!
