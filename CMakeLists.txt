cmake_minimum_required(VERSION 3.22)

project(emt-game LANGUAGES C CXX)

file(GLOB_RECURSE srcs ${CMAKE_CURRENT_SOURCE_DIR}/*.h ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

add_library(emt-game STATIC ${srcs})
target_include_directories(emt-game PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/srcs)

set_target_properties(emt-game PROPERTIES
    ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/$<CONFIG>
)
