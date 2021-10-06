cmake_minimum_required(VERSION 3.15)

project(TryOuts LANGUAGES CXX)

set (Boost_DEBUG ON)
include_directories(${Boost_INCLUDE_DIRS})

find_package(Boost REQUIRED COMPONENTS program_options)

if(NOT Boost_FOUND)
    message(FATAL_ERROR "Boost Not found")
endif()

add_executable(helloworld main.cpp)

target_link_libraries(helloworld PUBLIC Boost::program_options)
