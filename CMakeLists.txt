cmake_minimum_required(VERSION 3.25)

project(wxstatictest)

find_package(wxWidgets REQUIRED)
include(${wxWidgets_USE_FILE})

add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE ${wxWidgets_LIBRARIES} -static -lSM)
