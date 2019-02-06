cmake_minimum_required(VERSION [cmake version]) //let clion decide this usually
project(project_name) //let clion decide this usually

set(CMAKE_CXX_STANDARD [c++ version]) //let clion decide this usually

//Set the path variables here to find all the required development libraries.
set(SDL2_PATH "C:\\Users\\Lamim\\Documents\\Programming\\SDL2\\DevLibs\\SDL2-2.0.9\\x86_64-w64-mingw32")
set(SDL2_IMAGE_PATH "C:\\Users\\Lamim\\Documents\\Programming\\SDL2\\DevLibs\\SDL2_image-2.0.4\\x86_64-w64-mingw32")
set(SDL2_TTF_PATH "C:\\Users\\Lamim\\Documents\\Programming\\SDL2\\DevLibs\\SDL2_ttf-2.0.15\\x86_64-w64-mingw32")
set(SDL2_MIXER_PATH "C:\\Users\\Lamim\\Documents\\Programming\\SDL2\\DevLibs\\SDL2_mixer-2.0.4\\x86_64-w64-mingw32")

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/CMakeScripts)

find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)
find_package(SDL2_ttf REQUIRED)
find_package(SDL2_mixer REQUIRED)

include_directories(${SDL2_INCLUDE_DIR}
        ${SDL2_IMAGE_INCLUDE_DIR}
        ${SDL2_TTF_INCLUDE_DIR}
        ${SDL2_MIXER_INCLUDE_DIR})

add_executable(project_name main.cpp module.cpp module.h) //let clion decide this usually

target_link_libraries(RPG1 ${SDL2_LIBRARY}
        ${SDL2_IMAGE_LIBRARIES}
        ${SDL2_TTF_LIBRARIES}
        ${SDL2_MIXER_LIBRARIES})