cmake_minimum_required(VERSION 2.8.4)
set(CMAKE_TOOLCHAIN_FILE ${CMAKE_SOURCE_DIR}/cmake/ArduinoToolchain.cmake)
set(PROJECT_NAME SmartHouse)
project(${PROJECT_NAME})

set(${CMAKE_PROJECT_NAME}_SKETCH SmartHouse.ino)
generate_arduino_firmware(${CMAKE_PROJECT_NAME})
link_directories(${PROJECT_NAME}/libs)
add_subdirectory(screen_yellow_blue_bentley)
add_subdirectory(screen_yellow_blue_text)
add_subdirectory(wireless_send)
add_subdirectory(wireless_get)