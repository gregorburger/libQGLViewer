qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(overpainting viewer.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(overpainting Widgets OpenGL Xml)
target_link_libraries(overpainting ${OPENGL_LIBRARIES} QGLViewer)
