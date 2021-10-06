cmake_minimum_required(VERSION 3.15)

project(TryOuts LANGUAGES CXX)

find_package(Boost REQUIRED COMPONENTS program_options)

if(NOT Boost_FOUND)
    message(FATAL_ERROR "Boost Not found")
endif()

add_executable(helloworld main.cpp)

target_link_libraries(helloworld PUBLIC Boost::program_options)
