qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(simpleViewer main.cpp simpleViewer.cpp ${RC_SOURCES})
qt5_use_modules(simpleViewer Widgets OpenGL Xml)
target_link_libraries(simpleViewer ${OPENGL_LIBRARIES} QGLViewer)
