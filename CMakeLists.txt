cmake_minimum_required(VERSION 3.28)
project(OpenGLspinningCube)

set(CMAKE_CXX_STANDARD 17)

find_package(glfw3 3.3 REQUIRED)
include_directories(${GLFW_INCLUDE_DIRS})
find_package(GLEW REQUIRED)
include_directories(${GLEW_INCLUDE_DIRS})
find_package(OpenGL REQUIRED)

add_executable(OpenGLspinningCube main.cpp)

target_link_libraries(OpenGLspinningCube glfw GLEW::GLEW ${OPENGL_LIBRARIES})