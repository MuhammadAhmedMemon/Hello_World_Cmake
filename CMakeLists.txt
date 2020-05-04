Cmake_minimum_required(VERSION 3.15.3)
project(HelloWorld VERSION 1.0.0)

find_package(boost)

add_library(applibStatic STATIC foo.cpp)
add_library(applibDynamic SHARED foo.cpp)
add_executable(app main.cpp)
target_link_libraries(app applibStatic ${boost_LIBRARIES})
