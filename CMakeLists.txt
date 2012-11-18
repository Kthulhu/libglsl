set(CMAKE_INCLUDE_CURRENT_DIR ON)

find_package(GLEW REQUIRED)
find_package(OpenGL REQUIRED)

include_directories(${GLEW_INCLUDE_DIR})
include_directories(${OPENGL_INCLUDE_DIR})

set(CORELIBS ${OPENGL_LIBRARY} ${GLEW_LIBRARY} )

add_library(libglsl glsl.cpp)

target_link_libraries(libglsl ${CORELIBS} )