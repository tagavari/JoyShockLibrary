cmake_minimum_required (VERSION 3.12)

project ("JoyShockLibrary" CXX)

set(CMAKE_CXX_STANDARD 20)

include (cmake/LinuxConfig.cmake)
include (cmake/WindowsConfig.cmake)
include (cmake/MacConfig.cmake)

if (BUILD_SHARED_LIBS)
    set (JSL_PLATFORM_DEPENDENCY_VISIBILITY PRIVATE)
else ()
    set (JSL_PLATFORM_DEPENDENCY_VISIBILITY PUBLIC)
endif ()

add_subdirectory (JoyShockLibrary)
