qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(frameTransform frameTransform.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(frameTransform Widgets OpenGL Xml)
target_link_libraries(frameTransform ${OPENGL_LIBRARIES} QGLViewer)
