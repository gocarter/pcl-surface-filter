cmake_minimum_required(VERSION 3.3)

# set the project name
project(pcl-surface-filter VERSION 0.0.1)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(PCL 1.10.0 REQUIRED)

# add includes
include_directories(
    include
    ${PCL_INCLUDE_DIRS}
)

# add the executable
# TODO
add_executable(${PROJECT_NAME} src/main.cpp)

## Specify libraries to link a library or executable target against
target_link_libraries(${PROJECT_NAME}
    ${PCL_LIBRARIES}
)