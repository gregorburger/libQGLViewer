qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(constrainedCamera main.cpp constrainedCamera.cpp ${RC_SOURCES})
qt5_use_modules(constrainedCamera Widgets OpenGL Xml)
target_link_libraries(constrainedCamera ${OPENGL_LIBRARIES} QGLViewer)
