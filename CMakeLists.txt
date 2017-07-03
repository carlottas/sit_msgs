cmake_minimum_required(VERSION 2.8.3)
project(sit_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)


## Generate messages in the 'msg' folder
add_message_files(
  FILES
  SpatialAtom.msg
  SpatialRelationship.msg
  atom.msg
  EpisodicScoreItem.msg
  SemanticScoreItem.msg
  RetrievalSemantic.msg
  RetrievalEpisodic.msg
  retrievalAtom.msg
  geometricCharacteristic.msg
  objectPropertyRetrieval.msg
  
  
)

# Generate services in the 'srv' folder
add_service_files(
  FILES
  SemanticInterface.srv
  EpisodicInterface.srv
  ScoreInterface.srv

 

)

# Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES armor_msgs
   CATKIN_DEPENDS message_runtime
#  DEPENDS system_lib
)

###########
## Build ##
###########

include_directories(
  ${catkin_INCLUDE_DIRS}
)
