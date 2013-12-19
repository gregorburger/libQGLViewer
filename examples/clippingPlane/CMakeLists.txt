qt5_add_resources(RC_SOURCES../qglviewer)
add_executable(clippingPlane main.cpp clippingPlane.cpp ${RC_SOURCES})
qt5_use_modules(clippingPlane Widgets OpenGL Xml)
target_link_libraries(clippingPlane ${OPENGL_LIBRARIES} QGLViewer)
