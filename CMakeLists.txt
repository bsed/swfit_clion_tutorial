cmake_minimum_required(VERSION 3.5)
project(HelloSwift)

#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

#set(SOURCE_FILES main.cpp)
#add_executable(HelloSwift ${SOURCE_FILES} sources/main.swift)

set(CMAKE_VERBOSE_MAKEFILE TRUE)

add_custom_target(HelloSwift
    COMMAND /home/kelvin/swift/swift3/usr/bin/swift build
    WORKING_DIRECTORY ${CMAKE_SOURCE_DIR}
    SOURCES  Package.swift Sources/main.swift)