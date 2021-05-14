## Include this file if you want to use libb64
## in YOUR (Pico) project.

cmake_minimum_required(VERSION 3.12)

# Define libb64 as INTERFACE library
add_library(libb64 INTERFACE)

target_sources(libb64 INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/src/cdecode.c
    ${CMAKE_CURRENT_LIST_DIR}/src/cencode.c
)

target_include_directories(libb64 INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/include/
)
