# Create executable file
add_executable(${PROJECT_NAME} main.cpp)

# Move output to bin folder
set_target_properties(
  ${PROJECT_NAME}
  PROPERTIES RUNTIME_OUTPUT_DIRECTORY
             "${PROJECT_SOURCE_DIR}/bin"
)
