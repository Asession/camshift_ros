cmake_minimum_required(VERSION 2.8.3)
project(camshift)


find_package(catkin REQUIRED roscpp rospy cmake_modules message_generation std_msgs)

include_directories(
include
  ${catkin_INCLUDE_DIRS}
)

add_message_files(FILES TargetPositionSize.msg)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(
  CATKIN_DEPENDS roscpp rospy message_runtime std_msgs
)
