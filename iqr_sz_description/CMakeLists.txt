cmake_minimum_required(VERSION 3.0.2)
project(iqr_sz_description)

find_package(catkin REQUIRED COMPONENTS
  husky_description
  urdf
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES iqr_sz_description
#  CATKIN_DEPENDS husky_description urdf
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)