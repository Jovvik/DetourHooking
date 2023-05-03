cmake_minimum_required(VERSION 3.20)
project(DetourHooking)

set(CMAKE_CXX_STANDARD 23)

set(CMAKE_POSITION_INDEPENDENT_CODE ON)

add_library(DetourHooking SHARED Source/DetourHooking.cpp)
target_include_directories(DetourHooking PUBLIC include)

add_executable(DetourHookingExample Example/Main.cpp)
target_link_libraries(DetourHookingExample PUBLIC DetourHooking)
