#David - Project config file
#
#
cmake_minimum_required (VERSION 2.6)
project (wav_reader)
#set version number
set (wav_reader_VERSION_MAJOR 1)
set (wav_reader_VERSION_MINOR 0)
# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
  "${PROJECT_SOURCE_DIR}/wav_reader_config.h.in"
  "${PROJECT_BINARY_DIR}/wav_reader_config.h"
  )
# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
include_directories("${PROJECT_BINARY_DIR}")
#add the executable
add_executable(wav_reader wav_reader.c)

