project(helloeos)

set(EOSIO_WASM_OLD_BEHAVIOR "Off")
find_package(eosio.cdt)

add_contract( helloeos helloeos helloeos.cpp )
target_include_directories( helloeos PUBLIC ${CMAKE_SOURCE_DIR}/../include )
target_ricardian_directory( helloeos ${CMAKE_SOURCE_DIR}/../ricardian )