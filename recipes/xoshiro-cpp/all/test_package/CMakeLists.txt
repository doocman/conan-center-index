cmake_minimum_required(VERSION 3.8)
project(test_package LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)

find_package(xoshiro-cpp REQUIRED CONFIG)

add_executable(test_package test_package.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE xoshiro-cpp::xoshiro-cpp)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_${CMAKE_CXX_STANDARD})
