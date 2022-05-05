cmake_minimum_required(VERSION 3.1)

project(Fortune)

file(GLOB_RECURSE SRCS "src/*.cpp" "src/*.h")
get_filename_component(abs_path "${CMAKE_SOURCE_DIR}/src/FortuneAlgorithm/main.cpp" ABSOLUTE)
list(REMOVE_ITEM SRCS "${abs_path}")

include_directories(src/)

add_library(Fortune ${SRCS})
