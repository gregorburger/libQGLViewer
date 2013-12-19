qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(keyboardAndMouse main.cpp keyboardAndMouse.cpp ${RC_SOURCES})
qt5_use_modules(keyboardAndMouse Widgets OpenGL Xml)
target_link_libraries(keyboardAndMouse ${OPENGL_LIBRARIES} QGLViewer)
