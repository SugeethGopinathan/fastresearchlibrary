cmake_minimum_required(VERSION 2.8.6)
project(FriLibrary)

if(UNIX)
    add_definitions(-D__LINUX__)
elseif(WIN32)
    add_definitions(-DWIN32)
elseif(APPLE)
    add_definitions(-D__MACOS__)
elseif(QNX)  # unsupported?
    add_definitions(-D__NTO__)
endif(UNIX)

add_definitions(-fpermissive)

set(LIBRARIES pthread rt TypeIRML m dl stdc++)

add_subdirectory(src)
