cmake_minimum_required (VERSION 2.6)
project (gl-maze)
add_executable(gl-maze cube.c)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)

include_directories(${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS})
target_link_libraries(gl-maze ${OPENGL_LIBRARIES} ${GLUT_LIBRARY})

add_executable(spin spin.c)
target_link_libraries(spin ${OPENGL_LIBRARIES} ${GLUT_LIBRARY})

add_executable(texture texture.c stbinc.c)
target_link_libraries(texture ${OPENGL_LIBRARIES} ${GLUT_LIBRARY})
