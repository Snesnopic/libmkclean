project("mkclean" VERSION 0.9.0 LANGUAGES C CXX)

add_library("mkclean_lib" STATIC mkclean.c)

set_property(TARGET mkclean_lib PROPERTY C_STANDARD 20)

configure_file(mkclean_project.h.in mkclean_project.h)
target_include_directories("mkclean_lib" PRIVATE ${CMAKE_CURRENT_BINARY_DIR})

target_link_libraries("mkclean_lib" PUBLIC "matroska2" "ebml2" "corec")

add_subdirectory("regression")
