set(PROJECT_NAME ImGUITemplate)
set(EXEC_NAME imgui-exec)
set(LIB_NAME imgui-example)
set(TEST_NAME imgui-test)
set(IMGUI_LIB_NAME imgui-sfml-custom)

project (${PROJECT_NAME})
cmake_minimum_required (VERSION 3.5.1)

# set compiler flags
set (CMAKE_CXX_COMPILER=g++)
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIC -std=c++14 -g") #-pthread -Wall -Wextra -Werror -Wfatal-errors -pedantic -g")

find_package(SFML REQUIRED COMPONENTS graphics window system)
include_directories(${SFML_INCLUDE_DIR})
include_directories(ext)

# add the code
add_subdirectory(ext)
add_subdirectory(src)
add_subdirectory(test)
