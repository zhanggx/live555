cmake_minimum_required(VERSION 3.15)
project(WindowsAudioInputDevice)

set(CMAKE_CXX_STANDARD 14)

aux_source_directory(. DIR_HELLO_SRCS)

add_library(WindowsAudioInputDevice ${DIR_HELLO_SRCS})

add_executable(WindowsAudioInputDevice_mixer
        showAudioInputPorts.cpp
        WindowsAudioInputDevice_common.cpp
        WindowsAudioInputDevice_common.hh
        WindowsAudioInputDevice_mixer.cpp
        WindowsAudioInputDevice_mixer.hh)
add_executable(WindowsAudioInputDevice_noMixer
        showAudioInputPorts.cpp
        WindowsAudioInputDevice_common.cpp
        WindowsAudioInputDevice_common.hh
        WindowsAudioInputDevice_noMixer.cpp
        WindowsAudioInputDevice_noMixer.hh)
target_link_libraries(WindowsAudioInputDevice_mixer BasicUsageEnvironment groupsock liveMedia UsageEnvironment ws2_32.lib winmm.lib)
target_link_libraries(WindowsAudioInputDevice_noMixer BasicUsageEnvironment groupsock liveMedia UsageEnvironment ws2_32.lib winmm.lib)