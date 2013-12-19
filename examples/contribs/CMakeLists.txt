qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(contribs  ${RC_SOURCES})
qt5_use_modules(contribs Widgets OpenGL Xml)
target_link_libraries(contribs ${OPENGL_LIBRARIES} QGLViewer)
