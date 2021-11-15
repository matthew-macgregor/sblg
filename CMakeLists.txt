cmake_minimum_required(VERSION 3.10)

project(sblg-main)

#Using the FindEXPAT module:
#include(FindEXPAT)
#find_package(EXPAT REQUIRED)

find_package(expat CONFIG REQUIRED)

file(GLOB Sources "src/*.c")
add_executable(sblg ${Sources})
target_link_libraries(sblg PRIVATE expat::expat)

#Using the FindEXPAT module:
#target_link_libraries(sblg PUBLIC EXPAT::EXPAT)
