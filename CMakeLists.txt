cmake_minimum_required(VERSION 3.12)
project(Solitaire)

set(CMAKE_CXX_STANDARD 14)
find_package(OpenMP)


add_executable(Solitaire Solitaire.cpp Card.cpp Deck.cpp GameBoard.cpp Card.h Deck.h Gameboard.h)

if(OpenMP_CXX_FOUND)
    target_link_libraries(Solitaire PUBLIC OpenMP::OpenMP_CXX)
endif()