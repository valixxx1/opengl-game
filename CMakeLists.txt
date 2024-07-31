cmake_minimum_required(VERSION 3.30.0)
project(Game)

add_executable(game src/main.cpp)

add_subdirectory(glad)
add_subdirectory(glfw)

target_link_libraries(game PRIVATE glad)
target_link_libraries(game PRIVATE glfw)

target_include_directories(game PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/glfw/include)