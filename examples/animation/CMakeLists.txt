qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(animation animation.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(animation Widgets OpenGL Xml)
target_link_libraries(animation ${OPENGL_LIBRARIES} QGLViewer)
