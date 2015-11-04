cmake_minimum_required(VERSION 2.8.3)
project(sar_msgs)

find_package(catkin REQUIRED COMPONENTS std_msgs message_generation)


add_message_files(
  FILES
  SarTaskTypes.msg
  VictimAnswer.msg
  Victims.msg  
)

generate_messages(
    DEPENDENCIES
)

catkin_package(
    DEPENDS 
    CATKIN_DEPENDS std_msgs message_runtime# TODO
    INCLUDE_DIRS  ${catkin_INCLUDE_DIRS}
    LIBRARIES # TODO
)

#install(DIRECTORY include/${PROJECT_NAME}/
#  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
#  FILES_MATCHING PATTERN "*.h")