qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(standardCamera viewer.cpp main.cpp cameraViewer.cpp standardCamera.cpp ${RC_SOURCES})
qt5_use_modules(standardCamera Widgets OpenGL Xml)
target_link_libraries(standardCamera ${OPENGL_LIBRARIES} QGLViewer)
