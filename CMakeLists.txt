cmake_minimum_required(VERSION 3.15)

project(LogView)

find_package(OpenCV REQUIRED)
find_package(Boost COMPONENTS thread system filesystem REQUIRED)
find_package(ZLIB REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})
include_directories(${Boost_INCLUDE_DIR})
include_directories(${ZLIB_INCLUDE_DIR})

add_definitions(-Wall)

set(CMAKE_CXX_FLAGS "-g -O3 -msse2 -msse3")

add_executable(LogView 
    "src/LogView.cpp"
    "src/RawLogReader.cpp"
    "src/RawLogReader.h"
    "src/Resolution.h"
)

target_link_libraries(LogView
                      ${ZLIB_LIBRARY}
                      ${Boost_LIBRARIES}
                      ${OpenCV_LIBS})
