Cmake_minimum_required(VERSION 3.15.3)
project(HelloWorld VERSION 1.0.0)
set(src foo.cpp bar.cpp)
set(BOOST_LIB /boost/libs)


add_library(applibStatic STATIC ${src})
add_library(applibDynamic SHARED ${src})
add_executable(app main.cpp)
target_link_libraries(app applibStatic ${BOOST_LIB})
