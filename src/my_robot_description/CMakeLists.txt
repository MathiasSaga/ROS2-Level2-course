cmake_minimum_required(VERSION 3.8)
project(my_robot_description)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)

install(
  DIRECTORY urdf launch rviz
  DESTINATION share/${PROJECT_NAME}/
)

# ANY ROS2 PACKAGE THAT DOESNT NEED TO COMPILE C++ CODE, YOU CAN USE --SYMLINK-INSTALL ON
# SO YOU CAN USE COLCON BUILD --SYMLINK-INSTALL HERE TOO.

ament_package()
