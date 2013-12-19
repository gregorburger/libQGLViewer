qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(select select.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(select Widgets OpenGL Xml)
target_link_libraries(select ${OPENGL_LIBRARIES} QGLViewer)
