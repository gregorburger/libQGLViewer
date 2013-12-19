qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(keyFrames keyFrames.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(keyFrames Widgets OpenGL Xml)
target_link_libraries(keyFrames ${OPENGL_LIBRARIES} QGLViewer)
