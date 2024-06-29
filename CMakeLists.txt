cmake_minimum_required(VERSION 3.29)
set(CMAKE_CXX_STANDARD 17)
project(ompeval)

add_subdirectory(omp)

add_executable(test benchmark.cpp test.cpp)
target_link_libraries(test ompeval pthread)

install(TARGETS ompeval)