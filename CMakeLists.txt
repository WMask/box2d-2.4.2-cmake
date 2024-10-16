## Box2D v2.4.2 ##

cmake_minimum_required(VERSION 3.11)

project(Box2D-cmake)

set(CMAKE_CXX_STANDARD 11)

file(GLOB_RECURSE Box2D_SRC
	RELATIVE ${CMAKE_SOURCE_DIR} "box2d-src-v.2.4.2/src/*.cpp"
	RELATIVE ${CMAKE_SOURCE_DIR} "box2d-src-v.2.4.2/include/*.h"
)

add_library(Box2D STATIC ${Box2D_SRC})
target_compile_features(Box2D PUBLIC cxx_std_11)
