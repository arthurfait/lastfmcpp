cmake_minimum_required(VERSION 2.8)

project(support_json)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
add_library(${PROJECT_NAME} STATIC jsoncpp.cpp json/json.h)

target_include_directories(${PROJECT_NAME} PUBLIC
                            ${CMAKE_CURRENT_SOURCE_DIR})


project(support_uri)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/uriparser)
add_library(${PROJECT_NAME} STATIC uriparser/UriCodec.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC
                            ${CMAKE_CURRENT_SOURCE_DIR}/uriparser)


