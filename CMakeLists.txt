cmake_minimum_required(VERSION 3.15)
project(chat CXX)

find_package(Boost REQUIRED COMPONENTS system thread asio regex)

include_directories(${Boost_INCLUDE_DIRS})

SET(USED_LIBS ${Boost_SYSTEM_LIBRARY} ${Boost_THREAD_LIBRARY} ${Boost_REGEX_LIBRARY})

add_executable(${PROJECT_NAME}_client client/src/main.cpp)
target_link_libraries(${PROJECT_NAME}_client ${USED_LIBS})

add_executable(${PROJECT_NAME}_server server/src/main.cpp)
target_link_libraries(${PROJECT_NAME}_server ${USED_LIBS})
