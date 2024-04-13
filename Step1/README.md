### Bare minimum requirements

Only three lines need to be added:

- `cmake_minimum_required`: sets the minimum cmake version required to run this project.
- `project()`: Command to setup the project name. Should be called immediately after cmake_minimum_required.
- `add_executable`: tells CMake to create an executable using the specified source files.

#### How to run:

```
mkdir build
cd build
cmake ../Step1 # Creates makefile
cmake --build .
```