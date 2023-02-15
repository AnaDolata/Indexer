cmake_minimum_required(VERSION 3.19)
project(indexer C)

set(CMAKE_C_STANDARD 11)

add_executable(indexer main.c libs/word_struct.c libs/read_files/read_files.c libs/hash_table/hash_table.c libs/hash_with_linked_list/hash_with_linked_list.c libs/simple_array/simple_array.c)