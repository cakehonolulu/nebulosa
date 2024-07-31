cmake_minimum_required(VERSION 3.26)
project(nebulosa)

set(CMAKE_CXX_STANDARD 23)

find_package(SDL2 REQUIRED)

# Specify the main executable
add_executable(nebulosa)

add_subdirectory(src)

# Link the library to the main executable
target_link_libraries(nebulosa PRIVATE ${SDL2_LIBRARIES})

# Set include directories for the main executable
target_include_directories(nebulosa PRIVATE ${PROJECT_SOURCE_DIR}/include ${SDL2_INCLUDE_DIRS})