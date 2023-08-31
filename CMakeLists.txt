cmake_minimum_required(VERSION 3.0.2)
project(gridmap_sampler)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  grid_map_core
  grid_map_cv
  grid_map_filters
  grid_map_loader
  grid_map_msgs
  grid_map_octomap
  grid_map_ros
  grid_map_rviz_plugin
  grid_map_sdf
  grid_map_visualization
  geometry_msgs
  sensor_msgs
  cv_bridge
  octomap_msgs
  filters
)

catkin_package(
)

include_directories(
 include
 ${catkin_INCLUDE_DIRS}
)

add_executable(demo1 src/demo1.cpp)

target_link_libraries(demo1
  #${PCL_LIBRARIES}
  ${catkin_LIBRARIES}
)

