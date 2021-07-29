# Copyright 2021 Simon Batardiere.
# All Rights Reserved.
#
# This file is part of the web3cpp project which is licensed under the Apache
# License 2.0 (the "License"). You may not use this file except in compliance
# with the License. You can obtain a copy in the file LICENSE in the source
# distribution.

cmake_minimum_required(VERSION 3.13)

project(
	Web3cpp
	VERSION 0.1
	LANGUAGES CXX
)

option(${PROJECT_NAME}_ENABLE_TEST "Enable test coverage." ON)

if(CMAKE_SOURCE_DIR STREQUAL CMAKE_BINARY_DIR)
	message(FATAL_ERROR "In-source builds is not allowed.")
endif()

add_subdirectory(third-party)
add_subdirectory(source)
if(${PROJECT_NAME}_ENABLE_TEST)
	add_subdirectory(test)
endif()

