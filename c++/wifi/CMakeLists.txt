cmake_minimum_required(VERSION 2.8.4)
project(wifi)

if(NOT ${UNIX})
    message(FATAL_ERROR "This project is designed to be compiled on linux/*NIX based platforms.")
endif()

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES main.cpp)
add_executable(wifi ${SOURCE_FILES})

set_target_properties(wifi PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/build
)
