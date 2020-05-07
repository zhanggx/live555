cmake_minimum_required(VERSION 3.15)
project(groupsock)

set(CMAKE_CXX_STANDARD 14)

aux_source_directory(. DIR_HELLO_SRCS)
add_library(groupsock ${DIR_HELLO_SRCS})