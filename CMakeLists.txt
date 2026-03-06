cmake_minimum_required(VERSION 3.10)
project(mini_llm)


set(CMAKE_CXX_STANDARD 17)

include_directories(include)

find_package(BLAS REQUIRED)

add_executable(mini_llm
    src/main.cpp
    src/tensor.cpp
    src/model.cpp
    src/sampler.cpp
)

target_link_libraries(mini_llm ${BLAS_LIBRARIES})
