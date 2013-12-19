qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(cameraLight main.cpp cameraLight.cpp ${RC_SOURCES})
qt5_use_modules(cameraLight Widgets OpenGL Xml)
target_link_libraries(cameraLight ${OPENGL_LIBRARIES} QGLViewer)
