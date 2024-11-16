cmake_minimum_required(VERSION 3.26)
project(FSM CXX)
add_executable(FSM src/main.cpp)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add third-party libraries
add_subdirectory(thirdparty)

# Add an option to enable tests
option(BUILD_TESTS "Build tests" OFF)

if (BUILD_TESTS)
    enable_testing() # Enable CTest functionality
    add_subdirectory(tests) # Include tests
endif()
