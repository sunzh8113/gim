project(ConnectServer)
set(CMAKE_VERBOSE_MAKEFILE ON)
add_definitions("-Wall -pg -g")
include_directories(${PROJECT_SOURCE_DIR}/../efnfw)
link_directories(/usr/local/lib ../efnfw/lib) 
link_libraries(libefnfw.a jsoncpp pthread)
file(GLOB_RECURSE SRC_LIST call_push_test.cpp)
add_executable(bin/CallPushTest ${SRC_LIST})
