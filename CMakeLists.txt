cmake_minimum_required(VERSION 3.30)

project(AOC2015
        HOMEPAGE_URL https://github.com/soworksl2/AdventOfCode2015
        LANGUAGES C CXX)

    set(CMAKE_CXX_STANDARD 20)


#set pedantic outputs
if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -pedantic -Wall -Wextra")
elseif(CMAKE_C_COMPILER_ID MATCHES "MSVC")
    set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} /W4 /permissive-")
endif()


add_subdirectory(sow_std) #our standard library for this project, and who knows? probably or standard library in general.

add_subdirectory(day1)
add_subdirectory(day2)
add_subdirectory(day3)
add_subdirectory(day4)
add_subdirectory(day5)
add_subdirectory(day6)
