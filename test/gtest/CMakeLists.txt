project(gtest)
add_subdirectory(lib/googletest)

include_directories(${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})


add_executable(Google_Tests_run falgo_test.cpp ../gbenchmark/falgo_benchmark.cpp)

target_link_libraries(Google_Tests_run factoriallib_lib)
target_link_libraries(Google_Tests_run gtest gtest_main)