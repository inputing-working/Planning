cmake_minimum_required(VERSION 3.29.0)
project(Planning
        VERSION 0.0.1
        DESCRIPTION "a demo of cmake Planning"
        HOMEPAGE_URL "https://github.com/inputing-working/Planning"
        LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 17)
enable_testing()

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process)
set(PNC_Map_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map)
set(Show_Result_Dir ${CMAKE_SOURCE_DIR}/src/show_result)

set(EIGEN3_INCLUDE_DIR "D:/Project/Library/eigen-3.4.0")
list(APPEND CMAKE_MODULE_PATH "${EIGEN3_INCLUDE_DIR}/cmake")
message("CMAKE_MODULE_PATH = ${CMAKE_MODULE_PATH}")

find_package(Eigen3 3.4 REQUIRED)
if(TARGET Eigen3::Eigen)
        message(STATUS "******Eigen3 3.4 found in ${CMAKE_MODULE_PATH}******")
endif()

add_subdirectory(src)
add_subdirectory(test/map_test)