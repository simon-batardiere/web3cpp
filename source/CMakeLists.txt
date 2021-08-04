# Copyright 2021 Simon Batardiere.
# All Rights Reserved.
#
# This file is part of the web3cpp project which is licensed under the Apache
# License 2.0 (the "License"). You may not use this file except in compliance
# with the License. You can obtain a copy in the file LICENSE in the source
# distribution.

find_package(Boost REQUIRED)
add_library(web3cpp ../include/web3cpp/dummy.h dummy.cpp)
set_target_properties(web3cpp PROPERTIES CXX_STANDARD 17)
target_include_directories(
	web3cpp
	PUBLIC "${PROJECT_SOURCE_DIR}/include/web3cpp"
)

