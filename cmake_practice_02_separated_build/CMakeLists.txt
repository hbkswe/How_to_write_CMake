# -------------------------------------------
# The minimum version that required to be able to read this CMakeList.txt
# -------------------------------------------
cmake_minimum_required(VERSION 2.8.12)

# -------------------------------------------
# Project name often named as the binary (executable) file
# -------------------------------------------
project (helloworld)

# -------------------------------------
# declare the directories that store project's file headers (.h)
# -------------------------------------
include_directories(include)

# -------------------------------------
# adding source code file with command *set*
# -------------------------------------
# set(SOURCES source/mainapp.cpp source/greetings_english.cpp source/greetings_chinese.cpp source/greetings_vietnamese.cpp)

# -------------------------------------
# An alternative to set() is file(), this method is a good practice and
# saving developers time and also more common among developer community
# And also, it support glob *
# -------------------------------------
file(GLOB SOURCES "source/*.cpp")

# -------------------------------------------
# Define the relationship between the the source code and the binary file
# -------------------------------------------
add_executable(helloworld ${SOURCES})
