cmake_minimum_required(VERSION 3.18)
project (HELLO-LIB)

include(GNUInstallDirs)

add_library(HelloLib hello.cxx)

set_target_properties(HelloLib PROPERTIES PUBLIC_HEADER "libhello/hello.h")

target_include_directories (HelloLib PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/libhello)

install(TARGETS HelloLib
        PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_PREFIX}${CMAKE_INSTALL_OLDINCLUDEDIR})
