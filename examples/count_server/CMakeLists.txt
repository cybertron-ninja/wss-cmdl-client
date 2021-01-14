cmake_minimum_required(VERSION 3.15)
project(count_server)
set(CMAKE_CXX_STANDARD 11)

include_directories(/home/mellertson/Documents/Development_Projects/Open_Source_Projects/websocketpp)

add_executable(count_server count_server.cpp)

target_link_libraries(count_server boost_system pthread crypto ssl)
