cmake_minimum_required(VERSION 3.10)

project(SpaceInvader)

add_subdirectory(vendor/Glad)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(vendor/glfw)

add_executable(SpaceInvader src/main.cpp)
target_link_libraries(SpaceInvader glfw Glad)
target_include_directories(SpaceInvader PUBLIC vendor/glfw/include vendor/Glad/include)
