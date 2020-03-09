cmake_minimum_required(VERSION 2.8.11)
project(cmake_wrapper)

if(EXISTS "${CMAKE_BINARY_DIR}/conanbuildinfo.cmake")
  include("${CMAKE_BINARY_DIR}/conanbuildinfo.cmake")
else()
  include(conanbuildinfo.cmake)
endif()
conan_basic_setup()

set(CMAKE_CXX_STANDARD 11)
add_subdirectory("source_subfolder")
