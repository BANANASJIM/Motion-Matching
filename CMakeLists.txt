cmake_minimum_required(VERSION 3.2)
set(-DCMAKE_TOOLCHAIN_FILE=E:/dev/vcpkg/scripts/buildsystems/vcpkg.cmake)
project(motion-matching)

set(CMAKE_CXX_STANDARD 11)
find_package(raylib CONFIG REQUIRED)


include_directories("${PROJECT_SOURCE_DIR}")

aux_source_directory("${PROJECT_SOURCE_DIR}" SRCS)

add_executable(motion_matching "controller.cpp")

target_link_libraries(motion_matching PRIVATE raylib)

