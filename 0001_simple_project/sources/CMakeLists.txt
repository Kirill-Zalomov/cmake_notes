cmake_minimum_required(VERSION 3.5)

project(app LANGUAGES CXX VERSION 1.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
aux_source_directory(./ SOURCES)

add_executable(app ${SOURCES})
target_link_libraries(app libstdc++)



