cmake_minimum_required(VERSION 3.23)
set(CMAKE_CXX_STANDARD 20)

project(SeedrMan)

add_subdirectory(dependencies)

enable_testing()
add_subdirectory(test)

add_library(SeedrMan SHARED library.cpp)

