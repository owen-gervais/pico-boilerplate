cmake_minimum_required(VERSION 3.12)

# Pull in SDK (must be before the project)
include($ENV{PICO_SDK_PATH}/external/pico_sdk_import.cmake)

# Rename from boilerplate
project(boilerplate C CXX ASM)

# Intiailize the Pico SDK
pico_sdk_init()

# Add the executable to project
add_executable(${PROJECT_NAME} main.c)
target_link_libraries(${PROJECT_NAME} pico_stdlib)

# Create the UF2 output file
pico_add_extra_outputs(${PROJECT_NAME})


