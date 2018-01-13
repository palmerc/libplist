cmake_minimum_required(VERSION 3.9)

project( cnary )

set( SOURCE_FILES
    iterator.c
    list.c
    node.c
    node_iterator.c
    node_list.c )

add_library( cnary STATIC ${SOURCE_FILES} )
target_include_directories( cnary PUBLIC include )

add_executable( cnary-exe cnary.c )
set_target_properties( cnary-exe PROPERTIES
    OUTPUT_NAME cnary )
target_link_libraries( cnary-exe cnary )

install(TARGETS cnary-exe cnary
     RUNTIME DESTINATION bin
     ARCHIVE DESTINATION lib )
