cmake_minimum_required(VERSION 3.0.2)
project(robot_rms_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS std_msgs message_generation)


#######################################
## Declare ROS messages and services ##
#######################################
## Generate messages in the 'msg' folder
add_message_files(DIRECTORY msg
    FILES
    StateMachineStatus.msg
    RMSStatus.msg
)
## Generate added messages and services with any dependencies listed here
generate_messages(
DEPENDENCIES
   std_msgs  # Or other packages containing msgs
)

catkin_package(CATKIN_DEPENDS
  message_runtime
  std_msgs
)