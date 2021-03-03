cmake_minimum_required( VERSION 2.8 )
project( ch3_example )
set(CMAKE_CXX_FLAGS "-std=c++11")

find_package (Eigen3  REQUIRED NO_MODULE)

add_executable(coordinateTransform coordinateTransform.cpp )
target_link_libraries(coordinateTransform ${Pangolin_LIBRARIES} Eigen3::Eigen)

find_package(Pangolin REQUIRED)
include_directories(${Pangolin_INCLUDE_DIRS})
add_executable(plotTrajectory plotTrajectory.cpp)
target_link_libraries(plotTrajectory ${Pangolin_LIBRARIES} Eigen3::Eigen)
