cmake_minimum_required(VERSION 3.15)
project(mediaServer)

set(CMAKE_CXX_STANDARD 14)

aux_source_directory(. DIR_HELLO_SRCS)
add_executable(mediaServer ${DIR_HELLO_SRCS})
target_link_libraries(mediaServer BasicUsageEnvironment groupsock liveMedia UsageEnvironment WindowsAudioInputDevice ws2_32.lib)