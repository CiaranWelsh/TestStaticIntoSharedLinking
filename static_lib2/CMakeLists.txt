set(target StaticLib2)
add_library(${target} STATIC Hello2.h Hello2.cpp)

target_include_directories(${target} PRIVATE  ${CMAKE_CURRENT_SOURCE_DIR})

set_property(TARGET ${target} PROPERTY
        MSVC_RUNTIME_LIBRARY "MultiThreaded")

