# Start template code for modern OpenGL 

Code is based from  [learnopgl](https://learnopengl.com/)


# Prerequisites

* [CMake](https://cmake.org/)

## Windows

* install [vcpkg](https://github.com/Microsoft/vcpkg)  package manager for C++ libs on windows 

* install glfw3 via vcpkg
```
vcpkg install glfw3
```

* Build from Visual Studio via folder of top folder or command line.
```
devenv .
```

## Mac OS

* install [brew](https://brew.sh/)
```
brew install glfw3 
```

* build 
```
mkdir build
cd build
cmake ..
make
````


# Issues 

* some unknown build problem with **vcpkg** [link](https://developercommunity.visualstudio.com/content/problem/209503/parameter-name-pathvalue-cannot-be-null-parameter.html)
* build from commandline not working (can be me)
```
md build
cd build
cmake .. -DCMAKE_TOOL_CHAIN=..\..\vcpkg\scripts\buildsystems\vcpkg.cmake
...
..
CMake Error at CMakeLists.txt:4 (find_package):
  By not providing "Findglfw3.cmake" in CMAKE_MODULE_PATH this project has
  asked CMake to find a package configuration file provided by "glfw3", but
  CMake did not find one.

  Could not find a package configuration file provided by "glfw3" with any of
  the following names:

    glfw3Config.cmake
    glfw3-config.cmake

  Add the installation prefix of "glfw3" to CMAKE_PREFIX_PATH or set
  "glfw3_DIR" to a directory containing one of the above files.  If "glfw3"
  provides a separate development package or SDK, be sure it has been
  installed.


-- Configuring incomplete, errors occurred!
```