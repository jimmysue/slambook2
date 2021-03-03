cmake_minimum_required( VERSION 2.8 )
project( geometry )

# 添加Eigen头文件
find_package (Eigen3  REQUIRED NO_MODULE)
add_executable(eigenGeometry eigenGeometry.cpp)
target_link_libraries(eigenGeometry Eigen3::Eigen)
