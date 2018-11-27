cmake_minimum_required(VERSION 3.8.0)

project(libmhsupport LANGUAGES C CXX)

# Check Install Path
if(DEFINED CMAKE_INSTALL_PREFIX)
    message("Use ${CMAKE_INSTALL_PREFIX} as install path")
endif()

if(NOT CMAKE_BUILD_TYPE)
    message(STATUS "No build type selected, default is Release")
    set(CMAKE_BUILD_TYPE "Release")
endif()

add_subdirectory(cmake)
find_package(MHSupport REQUIRED PATHS ${CMAKE_BINARY_DIR} NO_DEFAULT_PATH)

include_directories(BEFORE libs)
add_subdirectory(libs)
