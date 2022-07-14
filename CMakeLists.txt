cmake_minimum_required(VERSION 3.17)
project(example)

set(CMAKE_CXX_STANDARD 20)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK REQUIRED gtk4-win32)

include_directories(${GTK_INCLUDE_DIRS})
link_directories(${GTK_LIBRARY_DIRS})
link_libraries(${GTK_LIBRARIES})

add_executable(example main.cpp)

