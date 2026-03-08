cmake_minimum_required(VERSION 3.20)
project(lmshader)

find_package(glfw REQUIRED)
find_package(glm REQUIRED)

add_library(lmshader src/shaders.cpp)

target_include_directories(lmshader PUBLIC include ${GLFW_INCLUDE_DIR} ${GLM_INCLUDE_DIR})

target_link_libraries(lmshader PUBLIC glfw glm)
