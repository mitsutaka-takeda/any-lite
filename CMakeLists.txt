# Copyright 2016 by Martin Moene
#
# https://github.com/martinmoene/any-lite
#
# This code is licensed under the MIT License (MIT).

cmake_minimum_required( VERSION 3.6 )

project( any_lite CXX )

option(AnyLite_Tests "Enable testing" OFF)

add_library(AnyLite INTERFACE)
add_library(AnyLite::AnyLite ALIAS AnyLite)

target_include_directories(
  AnyLite
  INTERFACE
  include/nonstd
  )

if(AnyLite_Tests)
  enable_testing()
  add_subdirectory( test )
endif()

#add_subdirectory( example )

# end of file
