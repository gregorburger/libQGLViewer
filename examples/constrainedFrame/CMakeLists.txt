qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(constrainedFrame main.cpp constrainedFrame.cpp ${RC_SOURCES})
qt5_use_modules(constrainedFrame Widgets OpenGL Xml)
target_link_libraries(constrainedFrame ${OPENGL_LIBRARIES} QGLViewer)
