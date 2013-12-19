set(QGL_HEADERS  qglviewer.h
	  camera.h
	  manipulatedFrame.h
	  manipulatedCameraFrame.h
	  frame.h
	  constraint.h
	  keyFrameInterpolator.h
	  mouseGrabber.h
	  quaternion.h
	  vec.h
	  domUtils.h
	  config.h)

set(SOURCES qglviewer.cpp
	  camera.cpp
	  manipulatedFrame.cpp
	  manipulatedCameraFrame.cpp
	  frame.cpp
	  saveSnapshot.cpp
	  constraint.cpp
	  keyFrameInterpolator.cpp
	  mouseGrabber.cpp
	  quaternion.cpp
	  vec.cpp)

set(UIS ImageInterface.ui)

option(QGLVIEWER_WITH_VECTOR_RENDERING "Compile with Vector Rendering support. Disalbe if you have compile errors in VRender\\" ON)
if (QGLVIEWER_WITH_VECTOR_RENDERING)

set(SOURCES ${SOURCES}
        VRender/BackFaceCullingOptimizer.cpp
        VRender/BSPSortMethod.cpp
        VRender/EPSExporter.cpp
        VRender/Exporter.cpp
        VRender/FIGExporter.cpp
        VRender/gpc.cpp
        VRender/ParserGL.cpp
        VRender/Primitive.cpp
        VRender/PrimitivePositioning.cpp
        VRender/TopologicalSortMethod.cpp
        VRender/VisibilityOptimizer.cpp
        VRender/Vector2.cpp
        VRender/Vector3.cpp
        VRender/NVector3.cpp
        VRender/VRender.cpp)

set(VRENDER_HEADERS
        VRender/AxisAlignedBox.h
        VRender/Exporter.h
        VRender/gpc.h
        VRender/NVector3.h
        VRender/Optimizer.h
        VRender/ParserGL.h
        VRender/Primitive.h
        VRender/PrimitivePositioning.h
        VRender/SortMethod.h
        VRender/Types.h
        VRender/Vector2.h
        VRender/Vector3.h
        VRender/VRender.h)

set(UIS ${UIS} VRenderInterface.ui)

else (QGLVIEWER_WITH_VECTOR_RENDERING)

add_definitions(-DNO_VECTORIAL_RENDER)

endif (QGLVIEWER_WITH_VECTOR_RENDERING)

qt5_wrap_ui(UI_HEADERS ${UIS})

set(HEADERS ${QGL_HEADERS} ${UI_HEADERS})

option(QGLVIEWER_STATIC "Compile QGLViewer Library static" OFF)
if (QGLVIEWER_STATIC)
    add_library(QGLViewer STATIC ${SOURCES} ${HEADERS})
else (QGLVIEWER_STATIC)
    add_library(QGLViewer SHARED ${SOURCES} ${HEADERS})
endif (QGLVIEWER_STATIC)

qt5_use_modules(QGLViewer Widgets OpenGL Xml)
target_link_libraries(QGLViewer ${OPENGL_LIBRARIES}) 
