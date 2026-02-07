

cmake_minimum_required(VERSION 3.10)
project(aula_cmake_c10)

add_library(my_math
         src/math.c
         )

add_library(my_info1
         src/infox.c
         )

add_executable(MeuExecutavel main.c)

target_include_directories(MeuExecutavel PRIVATE inc)

target_link_libraries(MeuExecutavel PRIVATE my_math my_info1)


