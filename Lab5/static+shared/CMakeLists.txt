cmake_minimum_required(VERSION 3.0)
project(lab5)

add_library(sharedLib SHARED ./source/block.c)

add_library(staticLib STATIC ./source/block.c)

add_executable(sharedOut ./program.c)
target_link_libraries(sharedOut sharedLib)

add_executable(staticOut ./program.c)
target_link_libraries(staticOut staticLib)
