# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

project ("CMakeProjectSDL")

project(CMakeProjectSDL)

cmake_policy(SET CMP0079 NEW)

list(APPEND CMAKE_PREFIX_PATH "C:\\Users\\jrn\\Source\\Repos\\CMakeProjectSDL" "C:\\Users\\jrn\\Source\\Dev\\SDL2")
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "C:\\Users\\jrn\\Source\\Repos\\CMakeProjectSDL")

find_package(SDL2 REQUIRED)
# find_file(SDL2_INCLUDE_DIR NAME SDL.h HINTS SDL2)
# find_library(SDL2_LIBRARY NAME SDL2)
include_directories(${SDL2_INCLUDE_DIRS})

# Include sub-projects.
add_subdirectory ("CMakeProjectSDL")

target_link_libraries(CMakeProjectSDL ${SDL2_LIBRARIES})