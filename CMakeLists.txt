# Specify the minimum required version of CMake
cmake_minimum_required(VERSION 3.10)

# Project name
project(calculator)

# Set the C++ standard to use
set(CMAKE_CXX_STANDARD 17)

# Add a static library target using the calc src file
add_library(calculator STATIC calculator.cpp)

# Add the executable target and its source files
add_executable(calculator_exec main.cpp)

# Link the exec with the calc lib
target_link_libraries(calculator_exec calculator)