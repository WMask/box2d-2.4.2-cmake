
cmake_minimum_required(VERSION 3.11)

set (CMAKE_CXX_STANDARD 11)

file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "box2d-src-v.2.4.2/src/**/*.cpp")
include_directories(${CMAKE_SOURCE_DIR})
add_library(Box2D STATIC ${SOURCES})
target_include_directories(Box2D PUBLIC ${CMAKE_SOURCE_DIR})
