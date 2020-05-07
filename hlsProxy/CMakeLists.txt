cmake_minimum_required(VERSION 3.15)
project(hlsProxy)

set(CMAKE_CXX_STANDARD 14)

aux_source_directory(. DIR_HELLO_SRCS)
add_executable(hlsProxy ${DIR_HELLO_SRCS})
target_link_libraries(hlsProxy BasicUsageEnvironment groupsock liveMedia UsageEnvironment WindowsAudioInputDevice ws2_32.lib)