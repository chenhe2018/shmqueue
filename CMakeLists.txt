cmake_minimum_required(VERSION 2.8)
project(shmqueue)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES src/main.cpp
        src/messagequeue.cpp
        src/messagequeue.h)
add_executable(shmqueue ${SOURCE_FILES})

add_executable(cli src/client.cpp 
        src/messagequeue.cpp
        src/messagequeue.h)
