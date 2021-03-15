cmake_minimum_required(VERSION 3.17)

project(tinyosc VERSION 1.0.0)

add_library(tinyosc STATIC
    tinyosc.c tinyosc.h
)
set_target_properties(tinyosc PROPERTIES PUBLIC_HEADER tinyosc.h)

include(GNUInstallDirs)

install(TARGETS tinyosc
    ARCHIVE  DESTINATION ${CMAKE_INSTALL_LIBDIR}
    LIBRARY  DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME  DESTINATION ${CMAKE_INSTALL_BINDIR}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
)