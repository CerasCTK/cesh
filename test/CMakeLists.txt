# Using FetchContent to install google test
include(FetchContent)

# Fetch google test with version 1.14
FetchContent_Declare(
  googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG v1.14.0
)

FetchContent_MakeAvailable(googletest)

# Set output test file name
set(TEST_OUTPUT cesh_test)

# Set all test files
set(TEST_FILES some_test.cpp)

# Create test executable file
add_executable(${TEST_OUTPUT} ${TEST_FILES})

# Link test output with google test
target_link_libraries(${TEST_OUTPUT} PRIVATE GTest::gtest_main)

include(GoogleTest)
gtest_discover_tests(${TEST_OUTPUT})
