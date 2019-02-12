cmake_minimum_required(VERSION 3.10)

project( DisplayImage )

find_package( OpenCV REQUIRED )
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_INCLUDE_HEADERS_IN_COMPILE_COMMANDS ON)

# Enable C++11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)

set(SORUCE_FILES
    src/main.cpp
    src/myClass.cpp
)

add_executable(DisplayImage ${SORUCE_FILES})

target_link_libraries(DisplayImage ${OpenCV_LIBS})
