cmake_minimum_required(VERSION 3.6...4.10)
project("mkclean" LANGUAGES C)

# compiler flags based on original meson setup
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)

# CMake project placed at the root of the sources
add_subdirectory("corec")
add_subdirectory("libebml2")
add_subdirectory("libmatroska2")
add_subdirectory("mkclean")
