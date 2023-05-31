cmake_minimum_required(VERSION 3.4)

project(Solver)

add_library(formatter_lib STATIC 
/Users/admin/lab03/formatter_lib/formatter.cpp)

include_directories(formatter_lib PUBLIC /Users/admin/lab03/formatter_lib)

add_library(formatter_ex_lib STATIC 
/Users/admin/lab03/formatter_ex_lib/formatter_ex.cpp)

include_directories(formatter_lib PUBLIC /Users/admin/lab03/formatter_ex_lib)

add_library(solver_lib STATIC /Users/admin/lab03/solver_lib/solver.cpp)

include_directories(solver_lib PUBLIC /Users/admin/lab03/solver_lib)

add_executable(solver_app 
/Users/admin/lab03/solver_application/equation.cpp)

target_link_libraries(formatter_ex_lib formatter_lib)

target_link_libraries(solver_app formatter_ex_lib)

target_link_libraries(solver_app solver_lib)


