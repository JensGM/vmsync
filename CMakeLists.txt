cmake_minimum_required(VERSION 2.8.12 FATAL_ERROR)
project(vmsync)
enable_language( CXX )
include( CheckCXXSourceCompiles )
include( CTest )

set( CMAKE_CXX_FLAGS "-std=c++11 ${warnings} ${CMAKE_CXX_FLAGS}" )

find_package(librsync REQUIRED)
include_directories(${librsync_INCLUDE_DIRS})

enable_testing()
add_subdirectory(src)
