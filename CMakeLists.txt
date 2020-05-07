cmake_minimum_required(VERSION 3.15)
project(live555)

set(CMAKE_CXX_STANDARD 14)
add_definitions(-DNO_OPENSSL)
include_directories(./
        ./BasicUsageEnvironment/include
        ./groupsock/include
        ./liveMedia/include
        ./mediaServer
        ./UsageEnvironment/include
        ./WindowsAudioInputDevice)

add_subdirectory(BasicUsageEnvironment)
add_subdirectory(groupsock)
add_subdirectory(hlsProxy)
add_subdirectory(liveMedia)
add_subdirectory(mediaServer)
add_subdirectory(proxyServer)
add_subdirectory(UsageEnvironment)
add_subdirectory(WindowsAudioInputDevice)

add_executable(testRTSPClient testProgs/testRTSPClient.cpp)
add_executable(testH264VideoStreamer testProgs/testH264VideoStreamer.cpp)
target_link_libraries(testRTSPClient BasicUsageEnvironment groupsock liveMedia UsageEnvironment WindowsAudioInputDevice ws2_32.lib)
target_link_libraries(testH264VideoStreamer BasicUsageEnvironment groupsock liveMedia UsageEnvironment WindowsAudioInputDevice ws2_32.lib)