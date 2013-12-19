qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(luxo main.cpp luxo.cpp ${RC_SOURCES})
qt5_use_modules(luxo Widgets OpenGL Xml)
target_link_libraries(luxo ${OPENGL_LIBRARIES} QGLViewer)
