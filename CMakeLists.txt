cmake_minimum_required(VERSION 3.12)
project(sdl_images)

set(CMAKE_CXX_STANDARD 17)

add_executable(sdl_images main.cpp)

# SDL2
set(SDL2_PATH "C:\\SDL2-2.0.9\\x86_64-w64-mingw32")

find_package(SDL2 REQUIRED)

include_directories(${SDL2_INCLUDE_DIR})

target_link_libraries(sdl_images ${SDL2_LIBRARY})

# add images
configure_file(images/stretch.bmp images/stretch.bmp COPYONLY)