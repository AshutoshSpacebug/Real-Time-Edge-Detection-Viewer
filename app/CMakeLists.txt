cmake_minimum_required(VERSION 3.22.1)
project("edgedetection")

# Your OpenCV path
set(OpenCV_DIR "/home/ashutosh/Downloads/opencv-4.10.0-android-sdk/OpenCV-android-sdk/sdk/native/jni")

find_package(OpenCV REQUIRED)

add_library(native-lib SHARED
        src/main/cpp/native-lib.cpp)

target_link_libraries(native-lib
        ${OpenCV_LIBS}
        log)
