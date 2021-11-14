cmake_minimum_required(VERSION 3.10)

project(sblg-main)

include(FindEXPAT)
find_package(EXPAT REQUIRED)
include_directories(${EXPAT_INCLUDE_DIRS})

file(GLOB Sources "src/*.c")
add_executable(sblg ${Sources})
target_link_libraries(sblg ${EXPAT_LIBRARIES})

