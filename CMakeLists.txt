cmake_minimum_required(VERSION 3.20)

project(udp_server)

set(udp_server main.cpp)

#source_group(source FILES ${${PROJECT_NAME}_SRC})

add_executable(main.exe main.cpp socket_wrapper.cpp socket.cpp)
target_link_libraries(main.exe ws2_32.lib)

#if(WIN32)
#  target_link_libraries(udp_server wsock32 ws2_32)
#endif()

