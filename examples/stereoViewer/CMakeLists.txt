qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(stereoViewer main.cpp stereoViewer.cpp ${RC_SOURCES})
qt5_use_modules(stereoViewer Widgets OpenGL Xml)
target_link_libraries(stereoViewer ${OPENGL_LIBRARIES} QGLViewer)
