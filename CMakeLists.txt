cmake_minimum_required(VERSION 3.9)

project(ConcurrentQueue VERSION 0.0.1 DESCRIPTION "Moody camels multiple producer multiple consumer queue.")

add_library(ConcurrentQueue INTERFACE)
target_sources(ConcurrentQueue INTERFACE
    $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}>/concurrentqueue.h
    $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}>/blockingconcurrentqueue.h
)

target_include_directories(ConcurrentQueue INTERFACE
    $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:${YOUR_INSTALL_DIR}/ConcurrentQueue>
)
