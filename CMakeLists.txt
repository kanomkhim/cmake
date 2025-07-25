# mkdir build & cd build & cmake -G "MinGW Makefiles" ..

set(CMAKE_C_COMPILER "C:/kanomKhim/winlibs/bin/gcc.exe")
set(CMAKE_CXX_COMPILER "C:/kanomKhim/winlibs/bin/g++.exe")

cmake_minimum_required(VERSION 3.31)

project(test1)

add_executable(test1 test1.cpp)
