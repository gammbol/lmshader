cmake_minimum_required(VERSION 3.20)
project(lmshader)

add_subdirectory(deps/glfw)
add_subdirectory(deps/glm)

add_library(lmshader src/shaders.cpp)

target_include_directories(lmshader PUBLIC include)

target_link_libraries(lmshader PUBLIC glfw glm)
