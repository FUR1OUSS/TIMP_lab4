cmake_minimum_required(VERSION 3.4)

project(HelloWorld)

add_library(formatter_lib STATIC formatter.cpp)

include_directories(formatter_lib PUBLIC formatter_lib)

add_library(formatter_ex_lib STATIC formatter_ex.cpp)

include_directories(formatter_lib PUBLIC formatter_ex_lib)

add_executable(hello hello_world.cpp)

target_link_libraries(formatter_ex_lib formatter_lib)

target_link_libraries(hello formatter_ex_lib)
