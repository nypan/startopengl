cmake_minimum_required(VERSION 3.0)
project(startopengl)

find_package(glfw3 REQUIRED)

add_executable(main main.cpp glad.c)
# C++11, c++14
target_compile_features(main PRIVATE cxx_lambda_init_captures)
target_include_directories(main PRIVATE ${CMAKE_CURRENT_LIST_DIR}/include)
target_link_libraries(main PRIVATE glfw)