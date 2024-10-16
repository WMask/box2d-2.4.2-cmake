
cmake_minimum_required(VERSION 3.11)

set(CMAKE_CXX_STANDARD 11)

file(GLOB_RECURSE Box2D_SRC RELATIVE ${CMAKE_SOURCE_DIR} "box2d-src-v.2.4.2/src/*.cpp")

add_library(Box2D STATIC ${SOURCES})
target_sources(Box2D PRIVATE ${Box2D_SRC})
target_include_directories(Box2D PUBLIC "${CMAKE_SOURCE_DIR}/box2d-src-v.2.4.2/include")
