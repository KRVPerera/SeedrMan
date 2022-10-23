cmake_minimum_required(VERSION 3.23)
set(CMAKE_CXX_STANDARD 20)

project(SeedrMan)

#set(CMAKE_EXPORT_COMPILE_COMMANDS ON) # does not produce the json file
#set(CMAKE_EXPORT_COMPILE_COMMANDS ON CACHE INTERNAL "")
include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
CONAN_BASIC_SETUP()

add_subdirectory(dependencies)

add_library(${PROJECT_NAME} STATIC src/library.cpp)
target_include_directories(${PROJECT_NAME} PRIVATE include)


enable_testing()
add_subdirectory(test)
