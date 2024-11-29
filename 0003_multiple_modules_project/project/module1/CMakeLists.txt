add_library(module1)

target_include_directories(module1 PUBLIC inc)

aux_source_directory(src MODULE_1_SOURCES)
target_sources(module1 PRIVATE ${MODULE_1_SOURCES})

target_link_libraries(module1 libstdc++)