cmake_minimum_required(VERSION 2.8.12.2)

project(COREPAL)

include_directories(${COREPAL_SOURCE_DIR}/inc)
include_directories(${COREPAL_SOURCE_DIR}/src)
include_directories(${COREPAL_SOURCE_DIR}/../inc)

add_compile_options(-gdwarf-3)
add_compile_options(-fexceptions)

add_subdirectory(src)

if(CLR_CMAKE_BUILD_TESTS)
  add_subdirectory(tests)
endif(CLR_CMAKE_BUILD_TESTS)

