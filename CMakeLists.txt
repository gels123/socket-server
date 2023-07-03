cmake_minimum_required(VERSION 3.10)
project(i-socket-server)

add_definitions(-D__STDC_NO_ATOMICS__=1)

set(CMAKE_C_FLAGS "-std=gnu99")

add_executable(testtcpsvr
        socket_server.c
        testtcpsvr.c)
target_link_libraries(testtcpsvr pthread)

add_executable(testtcpclient
        socket_server.c
        testtcpclient.c)
target_link_libraries(testtcpclient pthread)