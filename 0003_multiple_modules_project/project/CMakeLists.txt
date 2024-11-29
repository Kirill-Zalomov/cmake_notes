cmake_minimum_required(VERSION 3.11)

project(app LANGUAGES CXX VERSION 1.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_subdirectory(module1)
add_subdirectory(module2)
add_subdirectory(module3)

aux_source_directory(. SOURCES)

add_executable(app)
target_sources(app PRIVATE ${SOURCES})
target_link_libraries(app libstdc++ module1 module2 module3)
