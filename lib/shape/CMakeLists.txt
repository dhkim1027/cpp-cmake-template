file(GLOB_RECURSE SRC_FILES CONFIGURE_DEPENDS
  ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp
)

add_library(shape STATIC ${SRC_FILES})

target_include_directories(shape PUBLIC ${CMAKE_SOURCE_DIR}/include)

target_compile_options(shape PRIVATE -Wall -Werror)

target_compile_features(shape PRIVATE cxx_std_17)

include(FetchContent)

FetchContent_Declare(
  Fmt
  GIT_REPOSITORY "https://github.com/fmtlib/fmt"
  GIT_TAG "7.1.3"
  )
FetchContent_MakeAvailable(Fmt)

target_link_libraries(shape PRIVATE fmt)
