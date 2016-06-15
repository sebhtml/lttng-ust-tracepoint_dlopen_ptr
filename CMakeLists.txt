
cmake_minimum_required(VERSION 2.8.11)

project(
  ALIGNER
  )

include_directories(
  .
  )

add_library(
  aligner-lib
  SHARED
  aligner-lib.cpp
  tracepoints.cpp
  )

add_library(
  tester-lib
  SHARED
  tester-lib.cpp
  )

link_libraries(
  aligner-lib
  lttng-ust
  )

add_executable(
  aligner
  aligner.cpp
  )

add_executable(
  tester
  tester.cpp
  )

target_link_libraries(
  tester
  tester-lib
  )
