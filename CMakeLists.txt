cmake_minimum_required(VERSION 2.8.3)
project(dragonfly_speech_recognition)

find_package(catkin REQUIRED COMPONENTS
  # hmi_msgs
  message_generation
  rospy
  std_msgs
)

add_message_files(
  FILES
    Choice.msg
)

add_service_files(
  FILES
    GetSpeech.srv
)

generate_messages(
  DEPENDENCIES
    std_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES dragonfly_speech_recognition
  CATKIN_DEPENDS
    hmi_msgs
    message_runtime
    std_msgs
#  DEPENDS system_lib
)
