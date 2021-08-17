cmake_minimum_required(VERSION 3.0)
project(spidev-test VERSION 0.0.1)

add_definitions(-D_GNU_SOURCE)
add_compile_options(-O -Wall -Werror --std=gnu99)

add_executable(spidev_test spidev_test.c)
add_executable(spidev_fdx spidev_fdx.c)

install(TARGETS spidev_test RUNTIME DESTINATION usr/bin)
install(TARGETS spidev_fdx RUNTIME DESTINATION usr/bin)