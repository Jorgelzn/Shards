cmake_minimum_required(VERSION 3.10)

# Set the project name and version
project(Shards VERSION 1.0)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Source files
file(GLOB_RECURSE SOURCES
    "${CMAKE_SOURCE_DIR}/src/*.cpp"
    "${CMAKE_SOURCE_DIR}/src/glad.c"
)

# Add the executable
add_executable(myprogram ${SOURCES})

# Add include directory
target_include_directories(myprogram PRIVATE "${CMAKE_SOURCE_DIR}/include")
