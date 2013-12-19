qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(fastDraw main.cpp fastDraw.cpp ${RC_SOURCES})
qt5_use_modules(fastDraw Widgets OpenGL Xml)
target_link_libraries(fastDraw ${OPENGL_LIBRARIES} QGLViewer)
