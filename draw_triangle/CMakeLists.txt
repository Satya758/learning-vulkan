cmake_minimum_required(VERSION 3.15)
project(draw_triangle)

set(CMAKE_CXX_STANDARD 20)

find_package(Vulkan REQUIRED)

SET(glf_include "/usr/local/include" CACHE PATH "Location of Vulkan Include")
SET(glf_lib "/usr/local/lib" CACHE PATH "Location of Vulkan Library")

add_executable(draw_triangle main.cpp)
target_link_libraries(draw_triangle  glfw3 dl X11 GLU GL m pthread vulkan  Vulkan::Vulkan)