cmake_minimum_required(VERSION 2.8)
project(Hello CXX)

add_executable(Hello first.cpp)
target_link_libraries(Hello ${Boost_LIBRARIES})

set(Boost_USE_STATIC_LIBS OFF)
set(Boost_USE_MULTITHREADED OFF)
set(Boost_USE_STATIC_RUNTIME OFF)
find_package(Boost 1.46.0
	REQUIRED
	COMPONENTS system filesystem)

set(CMAKE_CXX_FLAGS "-Wall -Wextra -std=c++11 -pipe")
