cmake_minimum_required(VERSION 3.27)

project(modules_playground)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_EXPERIMENTAL_CXX_MODULE_CMAKE_API aa1f7df0-828a-4fcd-9afc-2dc80491aca7)

add_executable(mix_modules_include)
target_sources(mix_modules_include
    PUBLIC
    ${PROJECT_SOURCE_DIR}/main.cpp
    PUBLIC FILE_SET CXX_MODULES FILES
    ${PROJECT_SOURCE_DIR}/module.cpp
)
