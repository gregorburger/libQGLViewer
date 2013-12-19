qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(manipulatedFrame main.cpp manipulatedFrame.cpp ${RC_SOURCES})
qt5_use_modules(manipulatedFrame Widgets OpenGL Xml)
target_link_libraries(manipulatedFrame ${OPENGL_LIBRARIES} QGLViewer)
