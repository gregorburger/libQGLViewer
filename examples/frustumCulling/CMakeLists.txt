qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(frustumCulling main.cpp frustumCulling.cpp cullingCamera.cpp box.cpp ${RC_SOURCES})
qt5_use_modules(frustumCulling Widgets OpenGL Xml)
target_link_libraries(frustumCulling ${OPENGL_LIBRARIES} QGLViewer)
