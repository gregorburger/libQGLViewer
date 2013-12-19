qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(drawLight drawLight.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(drawLight Widgets OpenGL Xml)
target_link_libraries(drawLight ${OPENGL_LIBRARIES} QGLViewer)
