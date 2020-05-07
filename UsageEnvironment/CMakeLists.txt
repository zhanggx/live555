cmake_minimum_required(VERSION 3.15)
project(UsageEnvironment)

set(CMAKE_CXX_STANDARD 14)

aux_source_directory(. DIR_HELLO_SRCS)
add_library(UsageEnvironment ${DIR_HELLO_SRCS})