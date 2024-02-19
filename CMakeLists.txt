cmake_minimum_required(VERSION 2.8.3)
project(scale_truck_control_lane_detector)

set(ENABLE_DRAFT ON)

find_package(catkin REQUIRED
  COMPONENTS
    rospy 
    std_msgs
    message_generation
    scale_truck_control_msgs
)

# add_message_files(
#   FILES
#     LaneCoefs.msg
# )
# 
# generate_messages(
#   DEPENDENCIES
#     std_msgs
# )

catkin_package(
  CATKIN_DEPENDS
    rospy
    std_msgs
    scale_truck_control_msgs
)

catkin_install_python(
  PROGRAMS
    src/lane_detector
  DESTINATION
    ${CATKIN_PACKAGE_BIN_DESTINATION}
)
