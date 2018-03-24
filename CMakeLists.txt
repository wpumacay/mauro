
cmake_minimum_required( VERSION 3.0.0 )

set( CMAKE_CXX_STANDARD 11 )

find_package( OpenGL REQUIRED )
find_package( Threads REQUIRED )

set( MAURO_INCLUDE_DIRECTORIES
	 "${CMAKE_SOURCE_DIR}/lib/include/"
	 "${CMAKE_SOURCE_DIR}/ext/glfw/include"
	 "${CMAKE_BINARY_DIR}/ext/glad/include" )

message( "mauroInc: ${MAURO_INCLUDE_DIRECTORIES}" )

add_definitions( -DRESOURCES_PATH="${CMAKE_SOURCE_DIR}/res/" )

add_subdirectory( ext )
add_subdirectory( lib )
add_subdirectory( tests )
