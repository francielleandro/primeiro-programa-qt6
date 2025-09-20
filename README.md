## Compilar
    qmake -makefile hello.pro
    make


## Executar
    ./hello

ou


## Compilar
    cmake_minimum_required(VERSION 3.16)
    project(hello_qt LANGUAGES CXX)

    set(CMAKE_CXX_STANDARD 17)
    set(CMAKE_AUTOMOC ON)
    set(CMAKE_AUTORCC ON)
    set(CMAKE_AUTOUIC ON)

    find_package(Qt6 REQUIRED COMPONENTS Widgets)

    add_executable(hello main.cpp)
    target_link_libraries(hello Qt6::Widgets)


## Executar
    cmake -B build
    cmake --build build
    ./build/hello


