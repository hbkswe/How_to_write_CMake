# -------------------------------------------
# The minimum version that required to be able to read this CMakeList.txt
# -------------------------------------------
cmake_minimum_required(VERSION 2.8.12)
# -------------------------------------------
# Project name often named as the binary (executable) file
# -------------------------------------------
project (multilang_greetings)
# -------------------------------------
# declare the directories that store project's file headers (.h)
# -------------------------------------
include_directories(include)
# -------------------------------------
# Adding the needed source files
# -------------------------------------
file(GLOB SOURCES "source/*.cpp")
# -------------------------------------------
# Define which source files are include into the library
# Type of the library is STATIC
# name of the library can be differed from project name
# -------------------------------------------
add_library(greetings_encnvi STATIC ${SOURCES})
