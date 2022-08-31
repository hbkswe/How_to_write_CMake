# -------------------------------------------
# The minimum version that required to be able to read this CMakeList.txt
# -------------------------------------------
cmake_minimum_required(VERSION 2.8.12)

# -------------------------------------------
# Project name often named as the binary (executable) file
# -------------------------------------------
project(helloworld)

# -------------------------------------------
# Define the relationship between the the source code and the binary file
# -------------------------------------------
add_executable(helloworld mainapp.cpp)
