qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(multiView multiView.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(multiView Widgets OpenGL Xml)
target_link_libraries(multiView ${OPENGL_LIBRARIES} QGLViewer)
