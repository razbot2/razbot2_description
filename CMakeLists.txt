cmake_minimum_required(VERSION 2.8.3)
project(razbot2_description)
find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

# We add a roslaunch_add_file_check(...) macro that will do some basic validation on our launch files.
roslaunch_add_file_check(launch)

install(
  DIRECTORY launch meshes robots urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
