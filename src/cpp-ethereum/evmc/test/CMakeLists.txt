# EVMC: Ethereum Client-VM Connector API.
# Copyright 2018 The EVMC Authors.
# Licensed under the Apache License, Version 2.0. See the LICENSE file.

if(${CMAKE_SYSTEM_NAME} MATCHES "Linux")
    find_package(GTest REQUIRED)
else()
    find_package(GTest CONFIG REQUIRED)
endif()

if(NOT CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 11)
    set(CMAKE_CXX_EXTENSIONS OFF)
endif()

add_subdirectory(integration)
add_subdirectory(unittests)
add_subdirectory(vmtester)
