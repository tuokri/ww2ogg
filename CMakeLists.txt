cmake_minimum_required(VERSION 3.15)
project(ww2ogg)

set(CMAKE_CXX_STANDARD 20)

add_compile_options("/W4" "/std:c++latest"
        "$<$<CONFIG:RELEASE>:/O2;>")

add_executable(
        ww2ogg
        src/Bit_stream.h
        src/codebook.cpp
        src/codebook.h
        src/crc.c
        src/crc.h
        src/errors.h
        src/ww2ogg.cpp
        src/wwriff.cpp
        src/wwriff.h
)
