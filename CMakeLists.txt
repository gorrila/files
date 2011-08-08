# Check http://elementaryos.org/docs/developer-guide/cmake for documentation

cmake_minimum_required (VERSION 2.6)
cmake_policy(VERSION 2.6)
project(Marlin)
list(APPEND CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake/vala )
set(GETTEXT_PACKAGE "marlin")
set(PIXMAP_DIR "${CMAKE_INSTALL_PREFIX}/share/pixmaps/marlin/")
set(GNOMELOCALEDIR "${CMAKE_INSTALL_PREFIX}/share/locale/")
set(UI_DIR "${CMAKE_INSTALL_PREFIX}/share/marlin/ui/")
set(PACKAGE_VERSION 0.1)
set(VERSION 0.1)
configure_file (${CMAKE_SOURCE_DIR}/config.h.cmake ${CMAKE_BINARY_DIR}/config.h)
add_subdirectory (src)
add_subdirectory (data)
add_subdirectory (marlin-daemon)
add_subdirectory (icons)
add_subdirectory (libcore)
add_subdirectory (libwidgets)
add_subdirectory (plugins)
add_subdirectory (schemas)