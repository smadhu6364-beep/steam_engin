cmake_minimum_required(VERSION 3.16)
project(steam_engine LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(OpenGL_GL_PREFERENCE GLVND)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)

add_executable(steam_engine main.cpp)
target_link_libraries(steam_engine PRIVATE GLUT::GLUT OpenGL::GL OpenGL::GLU)

if(APPLE)
  # Apple's bundled GLUT and OpenGL are deprecated but still work
  target_compile_definitions(steam_engine PRIVATE GL_SILENCE_DEPRECATION)
endif()
