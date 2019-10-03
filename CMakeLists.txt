cmake_minimum_required(VERSION 2.8)
project(kcf_catkin)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

add_definitions(-fPIC -shared)

#############
# LIBRARIES #
#############
set(SOURCES
  src/fhog.cpp
  src/kcftracker.cpp
)

cs_add_library(${PROJECT_NAME} ${SOURCES})

##########
# EXPORT #
##########
cs_install()
cs_export(INCLUDE_DIRS src)
