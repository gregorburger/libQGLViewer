qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(screenCoordSystem screenCoordSystem.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(screenCoordSystem Widgets OpenGL Xml)
target_link_libraries(screenCoordSystem ${OPENGL_LIBRARIES} QGLViewer)
