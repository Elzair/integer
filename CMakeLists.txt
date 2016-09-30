cmake_minimum_required(VERSION 3.3)

project(boost_integer)

add_library(boost_integer INTERFACE)

target_include_directories(boost_integer BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_integer DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::integer ALIAS boost_integer)
