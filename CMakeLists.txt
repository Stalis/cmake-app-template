cmake_minimum_required(VERSION 3.13)
project(app C)

set(CMAKE_C_STANDARD 99)

file(GLOB SOURCES src/*.c)
file(GLOB HEADERS include/*.h)

add_executable(app ${HEADERS} ${SOURCES})
target_include_directories(app PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})