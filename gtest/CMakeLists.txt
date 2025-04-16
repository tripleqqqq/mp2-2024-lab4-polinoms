cmake_minimum_required(VERSION 3.10)
set(target gtest_lib)  

add_library(${target} STATIC 
    gtest-all.cc
    gtest.h
)

if(UNIX AND NOT APPLE)
    find_package(Threads REQUIRED)
    target_link_libraries(${target} Threads::Threads)
endif()