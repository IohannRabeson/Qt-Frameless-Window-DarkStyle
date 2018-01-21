cmake_minimum_required(VERSION 3.9)
project(QtDarkStyle)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt5Core)
find_package(Qt5Widgets)

set(QT_DARKSTYLE_SOURCE
    DarkStyle.h
    DarkStyle.cpp
    darkstyle.qrc)

add_library(QtFramelessWindowDarkStyle ${QT_DARKSTYLE_SOURCE})
target_link_libraries(QtFramelessWindowDarkStyle PRIVATE Qt5::Core Qt5::Widgets)
target_include_directories(QtFramelessWindowDarkStyle PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>)
