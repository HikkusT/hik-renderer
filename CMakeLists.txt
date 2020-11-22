cmake_minimum_required(VERSION 3.17)
project(hik_renderer)

set(CMAKE_CXX_STANDARD 17)
# Find out how to add O2 flag here
#set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -O2")

add_executable(hik_renderer main.cpp)

find_package(glfw3 REQUIRED)
find_package(Vulkan REQUIRED)
target_link_libraries(hik_renderer glfw Vulkan::Vulkan)