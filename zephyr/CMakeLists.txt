cmake_minimum_required(VERSION 3.13.1)
include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(PIO_L476RG_Dev LANGUAGES CXX)

#Specify the C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CONFIG_LIB_CPLUSPLUS ON)
set(CONFIG_NEWLIB_LIBC ON)

FILE(GLOB app_sources ../src/*.c*)
target_sources(app PRIVATE ${app_sources})