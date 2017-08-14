# imgui library

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS}  ${GLUT_INCLUDE_DIRS})

set(SOURCES imconfig.h
            imgui.h
            imgui.cpp
            imgui_draw.cpp
            imgui_demo.cpp
            imgui_internal.h
            stb_textedit.h
            stb_rect_pack.h
            stb_truetype.h
            imgui-sfml.h
            imgui-sfml.cpp)

add_library(${IMGUI_LIB_NAME} ${SOURCES})

target_link_libraries(${IMGUI_LIB_NAME} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES} ${OPENGL_LIBRARIES} ${GLUT_LIBRARY})
set_target_properties(${IMGUI_LIB_NAME} PROPERTIES LINKER_LANGUAGE CXX)
