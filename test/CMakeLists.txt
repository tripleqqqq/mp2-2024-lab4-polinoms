cmake_minimum_required(VERSION 3.10)
set(target polinoms_test_run) 

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/../include
    ${CMAKE_CURRENT_SOURCE_DIR}/../gtest
)

file(GLOB srcs "*.cpp" "../src/*.cpp")


add_executable(${target} ${srcs})

target_link_libraries(${target} gtest_lib)