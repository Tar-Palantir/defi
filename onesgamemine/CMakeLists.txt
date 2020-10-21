cmake_minimum_required(VERSION 3.15)

project(onesgamemine)

set(EOSIO_WASM_OLD_BEHAVIOR "Off")
find_package(eosio.cdt)

add_contract(onesgamemine onesgamemine ${CMAKE_CURRENT_SOURCE_DIR}/onesgamemine.cpp)

target_include_directories(onesgamemine PUBLIC )

set_target_properties(onesgamemine
        PROPERTIES
        RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}")

target_compile_options( onesgamemine PUBLIC )
