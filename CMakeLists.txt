cmake_minimum_required(VERSION 3.10)

# Program name
project(sfmlgame)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add sources
file(GLOB src "src/*.h" "src/*.cpp")
add_executable(${PROJECT_NAME} ${src})

# Add SFML
# set(SFML_STATIC_LIBRARIES TRUE)
add_subdirectory(ext/SFML)
target_link_libraries(${PROJECT_NAME} PRIVATE sfml-graphics)