cmake_minimum_required(VERSION 2.8.3)
project(robotis_controller_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  sensor_msgs
  std_msgs
  message_generation
)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  SyncWriteItem.msg
  JointCtrlModule.msg
  StatusMsg.msg
)

## Generate services in the 'srv' folder
add_service_files(
  FILES
  GetJointModule.srv
)
  #   Service1.srv
#   Service2.srv
# )

## Generate actions in the 'action' folder
# add_action_files(
#   FILES
#   Action1.action
#   Action2.action
# )

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  sensor_msgs
)

catkin_package(
#  INCLUDE_DIRS include
  CATKIN_DEPENDS sensor_msgs std_msgs
)

