cmake_minimum_required(VERSION 3.15)
project(liveMedia)

set(CMAKE_CXX_STANDARD 14)

aux_source_directory(. DIR_HELLO_SRCS)
add_library(liveMedia ${DIR_HELLO_SRCS})