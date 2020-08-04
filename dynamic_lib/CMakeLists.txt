set(target SharedLibrary)
add_library(${target} SHARED SharedHello.h SharedHello.cpp)
target_include_directories(${target} PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}
        ${CMAKE_SOURCE_DIR}/static_lib1
        ${CMAKE_SOURCE_DIR}/static_lib2
        )

target_link_libraries(${target} PRIVATE StaticLib1 StaticLib2)
add_dependencies(${target} StaticLib1 StaticLib2)


set_property(TARGET ${target} PROPERTY
        MSVC_RUNTIME_LIBRARY "MultiThreadedDLL")











