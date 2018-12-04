cmake_minimum_required(VERSION 3.12)
project(KernelProfiler)

set(CMAKE_CXX_STANDARD 14)

## Add Include Directories
# usr/local/cuda/include contains the OpenCL header files
include_directories(/usr/local/lib /usr/local/cuda/include)

## Add Lib directories
link_directories(/usr/local/cuda/lib64)

## Add Target Executables
add_executable(KernelProfiler main.cpp convolution.cpp)

## Link Libraries to Executables
target_link_libraries(KernelProfiler OpenCL)