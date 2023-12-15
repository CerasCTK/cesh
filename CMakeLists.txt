cmake_minimum_required(VERSION 3.27 FATAL_ERROR)
project(cesh LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(CMAKE_EXPORT_COMPILE_COMMANDS True)

enable_testing()

add_subdirectory(src)
add_subdirectory(test)
