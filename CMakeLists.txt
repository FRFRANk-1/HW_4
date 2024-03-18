set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

cmake_minimum_required(VERSION 3.5.0)
project(HW_4 VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

find_package( Opencv REQUIRED)
include_directories( ${OpenCV_INCLUDE_DIRS} ${CMAKE_SOURCE_DIR})

add_executable(HW_4 main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
