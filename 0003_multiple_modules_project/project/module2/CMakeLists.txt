add_library(module2)

target_include_directories(module2 PUBLIC inc)

aux_source_directory(src MODULE_2_SOURCES)
target_sources(module2 PRIVATE ${MODULE_2_SOURCES})

target_link_libraries(module2 libstdc++)