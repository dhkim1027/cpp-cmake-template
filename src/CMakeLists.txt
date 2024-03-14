file(GLOB_RECURSE SRC_FILES CONFIGURE_DEPENDS
  ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp
)

add_executable(hello ${SRC_FILES})
target_include_directories(hello PUBLIC ${CMAKE_SOURCE_DIR}/include)
