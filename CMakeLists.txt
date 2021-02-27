cmake_minimum_required(VERSION 3.19)
project(FastLZ C)

set(CMAKE_C_STANDARD 11)

include_directories(.)

add_executable(6pack
        examples/6pack.c
        fastlz.c
        fastlz.h
        )

add_executable(6unpack
        examples/6unpack.c
        fastlz.c
        fastlz.h
        )

add_executable(tests
        tests/refimpl.c
        tests/test_roundtrip.c
        fastlz.c
        fastlz.h
        )
