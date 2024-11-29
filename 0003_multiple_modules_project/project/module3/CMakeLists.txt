add_library(module3)

target_include_directories(module3 PUBLIC inc)

aux_source_directory(src MODULE_3_SOURCES)
target_sources(module3 PRIVATE ${MODULE_3_SOURCES})

target_link_libraries(module3 libstdc++)