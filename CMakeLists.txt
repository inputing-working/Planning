cmake_minimum_required(VERSION 3.29.0)
project(Planning
        VERSION 0.0.1
        DESCRIPTION "a demo of cmake Planning"
        HOMEPAGE_URL "https://github.com/inputing-working/Planning"
        LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process)
set(PNC_Map_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map)


add_subdirectory(src)