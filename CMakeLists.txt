# CMake minimum version
cmake_minimum_required(VERSION 3.16)

# Project name
project(raymarching-project VERSION 0.1.0 LANGUAGES C CXX)

# Copy resources to build
file(COPY resources DESTINATION ${CMAKE_BINARY_DIR})

# Add executable
add_executable(${PROJECT_NAME} src/main.c resources)

# Add raylib subdirectory for build
add_subdirectory(libraries/raylib)

# Link raylib
target_link_libraries(${PROJECT_NAME} raylib)