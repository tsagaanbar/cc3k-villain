cmake_minimum_required(VERSION 3.16)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(PROJECT_NAME cc3k-villain)

project(${PROJECT_NAME})

include_directories(
    ${PROJECT_SOURCE_DIR}
)

add_executable(
    cc3k
    ./main.cc
    ./control/src/game.cc	
    ./control/src/display.cc
    ./facilities/src/floor.cc 
    ./facilities/src/chamber.cc 
    ./facilities/src/path.cc
    ./characters/src/player_character.cc    
    ./characters/src/character.cc
    ./characters/src/races.cc
    ./basic/src/canvas.cc 
    ./basic/src/figures.cc
    ./items/src/gold.cc
    ./items/src/potion.cc
)

install(TARGETS cc3k DESTINATION ${PROJECT_SOURCE_DIR}/bin)
