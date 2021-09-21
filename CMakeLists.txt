cmake_minimum_required (VERSION 2.6)
project (SimpleSQLite C)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED TRUE)

if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -pedantic -Wall")
endif()

add_executable(simpleSQLite SQLite.c)

# >> cmake -DCMAKE_BUILD_TYPE=Debug ..