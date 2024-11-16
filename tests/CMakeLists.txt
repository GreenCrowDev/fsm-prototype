# Create the test executable
add_executable(my_tests test_main.cpp)
target_link_libraries(my_tests PRIVATE doctest)

# Register the executable with CTest
add_test(NAME MyTests COMMAND my_tests)