cmake_minimum_required(VERSION 3.11)

project(
	hello
	VERSION
	0.1.0
	LANGUAGES C CXX)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

set(CMAKE_CXX_STANDARD 20) 
set(CMAKE_CXX_FLAGS "-O2 -Wall") 

add_subdirectory(lib)
add_subdirectory(src)
add_subdirectory(tests)
