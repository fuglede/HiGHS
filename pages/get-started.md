---
permalink: /get-started/
---

## Download 

HiGHS can be cloned from the Edinburgh Research Group in Optimization ([ERGO](https://www.maths.ed.ac.uk/ERGO/)) [GitHub repository](https://www.github.com/ERGO-COde/HiGHS).

``` bash
git clone https://github.com/ERGO-Code/HiGHS.git
```

### Build HiGHS from source code using CMake

HiGHS uses CMake as a build system. The simplest setup is to create a
build folder (within the folder into which HiGHS has been downloaded)
and then build HiGHS within it. The name of the build folder is
arbitrary but, assuming it is HiGHS/build, the full sequence of
commands required is as follows

``` bash
cd HiGHS
mkdir build
cd build
cmake ..
make -j
```

On Linux (and MacOS?), this creates the executable `build/bin/highs`. On Windows?

### Test Build

To perform a quick test to see whether the compilation was successful, run ctest from within the build folder.

``` bash
ctest 
```

### Install

The default installation location may need administrative permissions. To install, after building and testing, run 

``` bash
make install
```

To install in a specified installation directory run CMake with the CMAKE_INSTALL_PREFIX flag set: 

``` bash
cmake -DCMAKE_INSTALL_PREFIX=/path/to/highs_install ..
make -j
make install
```
Note that the installation folder should not be a sub-folder of the build folder.