Cmake_minimum_required(VERSION 2.8)
set(sub ./subdir)
set(CMAKE_CXX_FLAGS "-std=c++11")
#add_compile_option()
add_library(hello STATIC ${sub}/hello.cpp ${sub}/hello.hpp )
add_executable(first main.cpp) #${sub}/hello.cpp ${sub}/hello.hpp)
target_link_libraries(first hello)
