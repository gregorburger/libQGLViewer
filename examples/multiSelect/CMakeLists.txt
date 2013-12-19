qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(multiSelect multiSelect.cpp object.cpp manipulatedFrameSetConstraint.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(multiSelect Widgets OpenGL Xml)
target_link_libraries(multiSelect ${OPENGL_LIBRARIES} QGLViewer)
