## Box2D v2.4.2 ##

cmake_minimum_required(VERSION 3.11)

project(Box2D)

file(GLOB_RECURSE Box2D_SRC1 RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "box2d-src-v.2.4.2/src/*.cpp")
file(GLOB_RECURSE Box2D_SRC2 RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "box2d-src-v.2.4.2/src/*.h")
file(GLOB_RECURSE Box2D_INC RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "box2d-src-v.2.4.2/include/*.h")

set(Box2D_ALL "${Box2D_SRC1};${Box2D_SRC2};${Box2D_INC}")

add_library(Box2D ${Box2D_ALL})
target_include_directories(Box2D PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} "box2d-src-v.2.4.2/include")
target_compile_features(Box2D PUBLIC cxx_std_11)
