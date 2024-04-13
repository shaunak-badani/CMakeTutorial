# TODO 1: Set the minimum required version of CMake to be 3.10
cmake_minimum_required(VERSION 3.10)

# TODO 2: Create a project named Tutorial
# project(Tutorial)

# TODO 7: Set the project version number as 1.0 in the above project command
project(Tutorial VERSION 1.0) # Set's the version number

# TODO 6: Set the variable CMAKE_CXX_STANDARD to 11
#         and the variable CMAKE_CXX_STANDARD_REQUIRED to True

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True) # Mentions that we need to use C++ 11

# TODO 8: Use configure_file to configure and copy TutorialConfig.h.in to
#         TutorialConfig.h
configure_file(TutorialConfig.h.in TutorialConfig.h) # Copies values from CMAKE file to a header file
# The template file was defined in .h.in

# TODO 3: Add an executable called Tutorial to the project
# Hint: Be sure to specify the source file as tutorial.cxx
add_executable(frogging tutorial.cxx)

# TODO 9: Use target_include_directories to include ${PROJECT_BINARY_DIR}
target_include_directories(frogging PUBLIC
                           "${PROJECT_BINARY_DIR}"
                           ) # Tells CMAKE where to look for header files
                            # In this case, we want to ask it to look for TutorialConfig.h
