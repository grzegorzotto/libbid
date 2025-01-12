cmake_minimum_required(VERSION 3.22)
project(LibBid C)

FILE(GLOB SOURCES src/*.c)

add_library(LibBid STATIC ${SOURCES})

target_compile_definitions(LibBid PRIVATE
    -DCALL_BY_REF=0
    -DGLOBAL_RND=0
    -DGLOBAL_FLAGS=0
    -DUNCHANGED_BINARY_FLAGS=0) # internal flags for LibBid