cmake_minimum_required(VERSION 3.29)
project(ompeval)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -Wall -Wpedantic")

add_subdirectory(omp)

add_executable(test benchmark.cpp test.cpp)
target_link_libraries(test ompeval pthread)

install(TARGETS ompeval)