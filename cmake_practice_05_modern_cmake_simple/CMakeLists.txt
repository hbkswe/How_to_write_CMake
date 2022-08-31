cmake_minimum_required(VERSION 3.16)

project(practice5
    VERSION 1.0
    LANGUAGES CXX
)

add_library(mylib my_library.cpp)

add_executable(practice5executable main.cpp)

target_link_libraries(practice5executable PRIVATE mylib)