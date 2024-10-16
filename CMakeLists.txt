## Box2D v2.4.2 ##

cmake_minimum_required(VERSION 3.11)

project(Box2D-cmake)

set(CMAKE_CXX_STANDARD 11)

set(SOURCES
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_broad_phase.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_chain_shape.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_circle_shape.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_collide_circle.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_collide_edge.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_collide_polygon.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_collision.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_distance.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_dynamic_tree.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_edge_shape.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_polygon_shape.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/collision/b2_time_of_impact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/common/b2_block_allocator.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/common/b2_draw.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/common/b2_math.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/common/b2_settings.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/common/b2_stack_allocator.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/common/b2_timer.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_body.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_chain_circle_contact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_chain_circle_contact.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_chain_polygon_contact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_chain_polygon_contact.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_circle_contact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_circle_contact.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_contact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_contact_manager.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_contact_solver.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_contact_solver.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_distance_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_edge_circle_contact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_edge_circle_contact.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_edge_polygon_contact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_edge_polygon_contact.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_fixture.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_friction_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_gear_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_island.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_island.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_motor_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_mouse_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_polygon_circle_contact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_polygon_circle_contact.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_polygon_contact.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_polygon_contact.h
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_prismatic_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_pulley_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_revolute_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_weld_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_wheel_joint.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_world.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/dynamics/b2_world_callbacks.cpp
  ${PROJECT_SOURCE_DIR}/box2d-src-v.2.4.2/src/rope/b2_rope.cpp
)

add_library(Box2D STATIC ${SOURCES})
target_compile_features(Box2D PUBLIC cxx_std_11)
