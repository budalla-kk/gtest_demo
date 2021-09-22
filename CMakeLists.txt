cmake_minimum_required(VERSION 3.20)
project(gtest_demo)

set(CMAKE_CXX_STANDARD 14)

set(SOURCE_FILES main.cpp)
add_executable(gtest_demo main.cpp main.cpp factoriallib/falgo.cpp factoriallib/falgo.h)
add_executable(factorials_run ${SOURCE_FILES})

include_directories(factoriallib)
add_subdirectory(factoriallib)
target_link_libraries(factorials_run factoriallib_lib)

add_subdirectory(test/gbenchmark)
add_subdirectory(test/gtest)