cmake_minimum_required(VERSION 3.2)
project(dlib_mnist)


set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")


include(/usr/local/lib/cmake/dlib/dlib.cmake)
add_executable(dlib_mnist01 src/mnist01.cpp)
add_executable(dlib_mnist02 src/mnist02.cpp)
target_link_libraries(dlib_mnist01 dlib::dlib)
target_link_libraries(dlib_mnist02 dlib::dlib)