cmake_minimum_required(VERSION 3.15)
project(echo_client)
set(CMAKE_CXX_STANDARD 11)

include_directories(/home/mellertson/Documents/Development_Projects/Open_Source_Projects/websocketpp)

add_executable(echo_client echo_client.cpp)

target_link_libraries(echo_client boost_system pthread crypto ssl)
