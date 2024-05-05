

cmake_minimum_required(VERSION 3.11)


# option(SPDLOG_ACTIVE_LEVEL "Debug" 4)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(cpp_base64)

add_library(cpp_base64 STATIC
    base64.cpp
)

target_include_directories(cpp_base64 PUBLIC .)
install(TARGETS cpp_base64
    DESTINATION ${CMAKE_INSTALL_LIBDIR}
)

# Install the header file
install(FILES base64.h
    DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/cpp_base64
)

# target_link_libraries(strace_parser ${EXTERNALS})
