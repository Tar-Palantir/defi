cmake_minimum_required(VERSION 3.15)

project(onesgamedivd)

set(EOSIO_WASM_OLD_BEHAVIOR "Off")
find_package(eosio.cdt)

add_contract(onesgamedivd onesgamedivd ${CMAKE_CURRENT_SOURCE_DIR}/onesgamedivd.cpp)

target_include_directories(onesgamedivd PUBLIC )

set_target_properties(onesgamedivd
        PROPERTIES
        RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}")

target_compile_options( onesgamedivd PUBLIC )
