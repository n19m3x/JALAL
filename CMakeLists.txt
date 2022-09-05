cmake_minimum_required(VERSION 3.10)

project(JALAL VERSION 1.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

configure_file(${PROJECT_SOURCE_DIR}/src/JalalConfig.h.in ${PROJECT_SOURCE_DIR}/src/JalalConfig.h)

add_executable(JALAL ${PROJECT_SOURCE_DIR}/src/Jalal.cpp)

target_include_directories(JALAL PUBLIC
                           "${PROJECT_BINARY_DIR}"
                           )
