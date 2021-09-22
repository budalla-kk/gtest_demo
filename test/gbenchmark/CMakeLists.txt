add_compile_definitions(GOOGLETEST_PATH=lib/googletest)

project(benchmarks)
add_subdirectory(lib/benchmark)


add_executable(google_benchmarks_run falgo_benchmark.cpp)


target_link_libraries(google_benchmarks_run factoriallib_lib)
target_link_libraries(google_benchmarks_run benchmark::benchmark)
