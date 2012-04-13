cmake_minimum_required(VERSION 2.8)
project(iniparser)

include(GnuInstallDirs)

add_library(iniparser SHARED
    src/iniparser.c
    src/dictionary.c
)

install(FILES src/iniparser.h src/dictionary.h
        DESTINATION include)
install(TARGETS iniparser
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
)
