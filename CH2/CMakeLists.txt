cmake_minimum_required( VERSION 2.8 )

project(HelloSLAM)

add_executable( mymy helloSLAM.cpp )
add_library( word libwordSLAM.cpp )
add_library( word_shared SHARED libwordSLAM.cpp )

add_executable( uselib uselib.cpp )
target_link_libraries( uselib word_shared)

