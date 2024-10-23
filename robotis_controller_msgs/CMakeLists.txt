cmake_minimum_required(VERSION 3.5)
project(robotis_controller_msgs)

find_package(ament_cmake REQUIRED)
find_package(std_msgs REQUIRED)
find_package(sensor_msgs REQUIRED)
find_package(rosidl_default_generators REQUIRED)

set(msg_files
  "msg/SyncWriteItem.msg"
  "msg/JointCtrlModule.msg"
  "msg/StatusMsg.msg"
  "msg/WriteControlTable.msg"
)

set(srv_files
  "srv/GetJointModule.srv"
  "srv/SetJointModule.srv"
  "srv/SetModule.srv"
  "srv/LoadOffset.srv"
)

rosidl_generate_interfaces(${PROJECT_NAME}
  ${msg_files}
  ${srv_files}
  DEPENDENCIES std_msgs sensor_msgs
)

ament_export_dependencies(rosidl_default_runtime)
ament_package()
