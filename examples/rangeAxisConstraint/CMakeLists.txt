qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(rangeAxisConstraint rangeAxisConstraint.cpp viewer.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(rangeAxisConstraint Widgets OpenGL Xml)
target_link_libraries(rangeAxisConstraint ${OPENGL_LIBRARIES} QGLViewer)
