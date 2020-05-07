cmake_minimum_required(VERSION 3.15)
project(proxyServer)

set(CMAKE_CXX_STANDARD 14)

aux_source_directory(. DIR_HELLO_SRCS)
add_executable(proxyServer ${DIR_HELLO_SRCS})
target_link_libraries(proxyServer BasicUsageEnvironment groupsock liveMedia UsageEnvironment WindowsAudioInputDevice ws2_32.lib)