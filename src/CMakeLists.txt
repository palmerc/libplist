cmake_minimum_required(VERSION 3.9)

set( C_HEADER_FILES
    base64.h
    bytearray.h
    hashtable.h
    plist.h
    ptrarray.h
    strbuf.h
    time64.h
    time64_limits.h )

set( C_SOURCE_FILES
    base64.c
    bplist.c
    bytearray.c
    hashtable.c
    plist.c
    ptrarray.c
    time64.c
    xplist.c )

set( CXX_SOURCE_FILES
    Array.cpp
    Boolean.cpp
    Data.cpp
    Date.cpp
    Dictionary.cpp
    Integer.cpp
    Key.cpp
    Node.cpp
    Real.cpp
    String.cpp
    Structure.cpp
    Uid.cpp )

add_library( plist ${C_SOURCE_FILES} )
target_include_directories( plist PRIVATE ${CMAKE_CURRENT_SOURCE_DIR} )
target_link_libraries( plist cnary )
add_library( plist++ ${CXX_SOURCE_FILES} )

