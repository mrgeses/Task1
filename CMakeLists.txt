cmake_minimum_required(VERSION 3.14)

project(Task1)

add_library(Task1Lib SHARED Task1/Trigonometry.cpp Task1/Logic.cpp Task1/Piecewise.cpp Task1/Inside.cpp)

add_executable(Task1Tests Task1.Tests/Trigonometry.Tests.cpp Task1.Tests/Logic.Tests.cpp Task1.Tests/Piecewise.Tests.cpp Task1.Tests/Inside.Tests.cpp)

target_link_libraries(Task1Tests Task1Lib gtest_main gtest pthread)