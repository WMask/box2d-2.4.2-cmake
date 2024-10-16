## Box2D v2.4.2 ##

cmake_minimum_required(VERSION 3.11)

project(box2d
		VERSION 2.4.2
		LANGUAGES C CXX
)

file(GLOB_RECURSE box2d_SRC1 RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "box2d-src-v.2.4.2/src/*.cpp")
file(GLOB_RECURSE box2d_SRC2 RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "box2d-src-v.2.4.2/src/*.h")
file(GLOB_RECURSE box2d_INC RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "box2d-src-v.2.4.2/include/*.h")

set(box2d_ALL "${box2d_SRC1};${box2d_SRC2};${box2d_INC}")
set(box2d_INC_DIR "${CMAKE_CURRENT_SOURCE_DIR}/box2d-src-v.2.4.2/include")

add_library(box2d ${box2d_ALL})
target_include_directories(box2d PUBLIC ${box2d_INC_DIR})
target_compile_features(box2d PUBLIC cxx_std_11)
