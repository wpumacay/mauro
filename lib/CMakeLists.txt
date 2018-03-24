
message( "MAURO> CONFIGURING LIBRARY" )

include_directories( ${MAURO_INCLUDE_DIRECTORIES} )

## Configure library *****************************************

FILE( GLOB_RECURSE MauroSources src *.cpp )

add_library( mauro
             ${MauroSources} )

target_link_libraries( mauro
                       glfw glad
                       ${OPENGL_LIBRARIES}
                       ${CMAKE_THREAD_LIBS_INIT} )