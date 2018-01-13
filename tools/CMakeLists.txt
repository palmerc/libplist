
add_executable( plistutil plistutil.c )
target_link_libraries( plistutil plist )
target_include_directories( plistutil PRIVATE ${CMAKE_SOURCE_DIR}/include )
install( TARGETS plistutil
    RUNTIME DESTINATION bin )
