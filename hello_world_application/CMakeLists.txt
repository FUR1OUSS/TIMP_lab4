cmake_minimum_required(VERSION 3.4)

project(HelloWorld)

add_library(formatter_lib STATIC 
/Users/admin/lab03/formatter_lib/formatter.cpp)

include_directories(formatter_lib PUBLIC /Users/admin/lab03/formatter_lib)

add_library(formatter_ex_lib STATIC 
/Users/admin/lab03/formatter_ex_lib/formatter_ex.cpp)

include_directories(formatter_lib PUBLIC /Users/admin/lab03/formatter_ex_lib)

add_executable(hello 
/Users/admin/lab03/hello_world_application/hello_world.cpp)

target_link_libraries(formatter_ex_lib formatter_lib)

target_link_libraries(hello formatter_ex_lib)


