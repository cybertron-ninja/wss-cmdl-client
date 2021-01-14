# cmake_minimum_required(VERSION 3.15)
cmake_minimum_required(VERSION 3.13.4)
project(wss)
set(CMAKE_CXX_STANDARD 11)

include_directories(/home/mellertson/Documents/Development_Projects/Open_Source_Projects/websocketpp)

add_executable(wss main.cpp)

target_link_libraries(wss boost_system pthread crypto ssl)
