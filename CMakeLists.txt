cmake_minimum_required (VERSION 3.8)

project(BZ)
set(CMAKE_CXX_STANDARD 20)

link_directories(${CMAKE_SOURCE_DIR}/Dependencies/lib)

file(GLOB_RECURSE SOURCE_FILES 
	${CMAKE_SOURCE_DIR}/src/*.c
	${CMAKE_SOURCE_DIR}/src/*.cpp)

file(GLOB_RECURSE HEADER_FILES 
	${CMAKE_SOURCE_DIR}/Dependencies/*.h
	${CMAKE_SOURCE_DIR}/Dependencies/*.hpp)

add_executable(${PROJECT_NAME} ${HEADER_FILES} ${SOURCE_FILES})
