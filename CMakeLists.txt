cmake_minimum_required(VERSION 3.25)

project(wxstatictest)

set(wxWidgets_USE_DEBUG OFF)
set(wxWidgets_USE_STATIC ON)
find_package(wxWidgets REQUIRED)
include(${wxWidgets_USE_FILE})

add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE ${wxWidgets_LIBRARIES})
