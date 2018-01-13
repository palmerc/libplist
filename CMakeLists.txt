cmake_minimum_required(VERSION 3.9)

project( plist )

add_subdirectory( src )
add_subdirectory( libcnary )
add_subdirectory( tools )

target_include_directories( plist PUBLIC include )
target_include_directories( plist++ PUBLIC include )
