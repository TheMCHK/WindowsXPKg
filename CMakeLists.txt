cmake_minimum_required(VERSION 3.13)
project(WindowsXPKg)

find_package(OpenSSL 1.1 REQUIRED COMPONENTS Crypto)

add_executable(WindowsXPKg main.c)
target_link_libraries(WindowsXPKg PUBLIC OpenSSL::Crypto)
install(TARGETS WindowsXPKg)

add_executable(Srv2003KG Srv2003KGmain.c)
target_link_libraries(Srv2003KG PUBLIC OpenSSL::Crypto)
install(TARGETS Srv2003KG)
