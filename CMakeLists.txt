cmake_minimum_required(VERSION 2.8)

project(tlpb)

enable_testing()

add_subdirectory(lib)
add_subdirectory(threads)
add_subdirectory(sockets)
add_subdirectory(procexec)
#add_subdirectory(libbar)
