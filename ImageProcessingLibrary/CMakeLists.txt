cmake_minimum_required(VERSION 3.10)
project(ImageProcessingLibrary)

set(CMAKE_CXX_STANDARD 17)

# Find OpenCV
find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})

# Add source files
file(GLOB SOURCES "src/*.cpp")

add_executable(ImageProcessor ${SOURCES})
target_link_libraries(ImageProcessor ${OpenCV_LIBS})
