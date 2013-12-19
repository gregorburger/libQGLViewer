project(QGLViewer)

cmake_minimum_required(VERSION 2.6)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

find_package(Qt5Widgets REQUIRED)
find_package(Qt5OpenGL REQUIRED)
find_package(Qt5Xml REQUIRED)
find_package(OpenGL REQUIRED)
link_libraries(${OpenGL_LIBRARY_DIR})

add_subdirectory(QGLViewer)

option(WITH_EXAMPLES "Compile QGLViewer examples." ON)
if (WITH_EXAMPLES)
    add_subdirectory(examples)
endif (WITH_EXAMPLES)
