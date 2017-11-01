project( step2stl )
cmake_minimum_required( VERSION 3.0 )

add_definitions ( -Wall )

#set additionnal CMake module path
set( CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/")

find_package(OpenCascade REQUIRED)

include_directories ( SYSTEM
  ${OpenCASCADE_INCLUDE_DIR}
)

include_directories (
  ${CMAKE_SOURCE_DIR}
)

# # CMake summary
# message (STATUS "CMAKE_BUILD_TYPE: ${CMAKE_BUILD_TYPE}")

# Add your project files
file(GLOB SRCFILES *.cpp)
add_executable(${PROJECT_NAME}_bin ${SRCFILES})
target_link_libraries(${PROJECT_NAME}_bin ${OpenCASCADE_LIBRARIES})
