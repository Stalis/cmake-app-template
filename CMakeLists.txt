cmake_minimum_required(VERSION 3.13 FATAL_ERROR)
project(app C)

set(CMAKE_C_STANDARD 99)
set(LIBS_PATH ${CMAKE_CURRENT_SOURCE_DIR}/lib)

file(GLOB SOURCES src/*.c)
file(GLOB HEADERS include/*.h)

add_subdirectory(lib/mylib)

add_executable(app ${HEADERS} ${SOURCES})
target_link_libraries(app PRIVATE mylib)
target_include_directories(app PRIVATE ${CMAKE_CURRENT_SOURCE_DIR} ${LIBS_PATH}/cmake-lib-template)