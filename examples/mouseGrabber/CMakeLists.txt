qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(mouseGrabber mouseGrabber.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(mouseGrabber Widgets OpenGL Xml)
target_link_libraries(mouseGrabber ${OPENGL_LIBRARIES} QGLViewer)
