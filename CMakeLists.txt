cmake_minimum_required(VERSION 3.10)

set( CXXFLAGS "-g")

project(helfy)

set(CMAKE_CXX_STANDARD 14)

find_package(JNI REQUIRED)

include_directories(${JNI_INCLUDE_DIRS} )

add_library(MethodEntry SHARED
   test/one/helfy/native/MethodEntry.c
   )

target_link_libraries(MethodEntry ${JNI_LIBRARIES})
