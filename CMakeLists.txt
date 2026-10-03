cmake_minimum_required(VERSION 3.30)
project(KursovaCPP)

set(CMAKE_CXX_STANDARD 17)

add_executable(KursovaCPP main.cpp
        CUser.cpp
        CUser.h
        CProduct.cpp
        CProduct.h
        Catalog.cpp
        Catalog.h
        CAdmin.cpp
        CAdmin.h
        CBuyer.cpp
        CBuyer.h)

# Copy data files to build directory
add_custom_command(TARGET KursovaCPP POST_BUILD
    COMMAND ${CMAKE_COMMAND} -E copy
    ${CMAKE_SOURCE_DIR}/users.txt
    ${CMAKE_BINARY_DIR}/users.txt)

add_custom_command(TARGET KursovaCPP POST_BUILD
    COMMAND ${CMAKE_COMMAND} -E copy
    ${CMAKE_SOURCE_DIR}/products.txt
    ${CMAKE_BINARY_DIR}/products.txt)
