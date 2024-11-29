cmake_minimum_required(VERSION 3.11)

project(app LANGUAGES CXX VERSION 1.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories("inc")
aux_source_directory("src" SOURCES)

add_executable(app)
target_sources(app PRIVATE ${SOURCES})
target_link_libraries(app libstdc++)
