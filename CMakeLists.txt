cmake_minimum_required(VERSION 3.0)
project(winapp)

find_package(glfw3 REQUIRED)

add_executable(main main.cpp glad.c)
target_include_directories(main PRIVATE ${CMAKE_CURRENT_LIST_DIR}/include)
target_link_libraries(main PRIVATE glfw)