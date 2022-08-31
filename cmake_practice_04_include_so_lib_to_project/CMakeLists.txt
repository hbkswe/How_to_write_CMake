# -------------------------------------------
# The minimum version that required to be able to read this CMakeList.txt
# -------------------------------------------
cmake_minimum_required(VERSION 2.8.12)
# -------------------------------------------
# Project name often named as the binary (executable) file
# -------------------------------------------
project (multilang_greetings)
# -------------------------------------
# declare the directories that store the library (.so)
# -------------------------------------
set (PROJECT_LINK_LIBS libgreetings_encnvi.so)
link_directories(lib)
# -------------------------------------
# declare the directories that store project's file headers (.h)
# -------------------------------------
include_directories(include)
# -------------------------------------
# Adding the needed source files
# -------------------------------------
file(GLOB SOURCES "source/*.cpp")
# -------------------------------------------
# Define the relationship between the the source code and the binary file
# -------------------------------------------
add_executable(helloworld_in_4lang ${SOURCES})
# -------------------------------------------
# Needed library is declared via PROJECT_LINK_LIBS
# -------------------------------------------
target_link_libraries(helloworld_in_4lang ${PROJECT_LINK_LIBS})
