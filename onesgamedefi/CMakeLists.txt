cmake_minimum_required(VERSION 3.15)

project(onesgamedefi)

set(EOSIO_WASM_OLD_BEHAVIOR "Off")
find_package(eosio.cdt)

add_contract(onesgamedefi onesgamedefi ${CMAKE_CURRENT_SOURCE_DIR}/onesgamedefi.cpp)

target_include_directories(onesgamedefi PUBLIC )

set_target_properties(onesgamedefi
        PROPERTIES
        RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}")

target_compile_options( onesgamedefi PUBLIC )
