qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(callback callback.cpp main.cpp ${RC_SOURCES})
qt5_use_modules(callback Widgets OpenGL Xml)
target_link_libraries(callback ${OPENGL_LIBRARIES} QGLViewer)
