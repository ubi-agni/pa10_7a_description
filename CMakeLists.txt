cmake_minimum_required(VERSION 3.0.2)
project(pa10_7a_description)


find_package(catkin REQUIRED COMPONENTS
  xacro
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES pa10_7a_description
#  CATKIN_DEPENDS xacro
#  DEPENDS system_lib
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)


#############
## Install ##
#############

foreach(dir config launch urdf meshes robots)
   install(DIRECTORY ${dir}/
      DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)
