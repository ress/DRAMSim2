project(dramsim2)
INCLUDE("${esesc_SOURCE_DIR}/CMake.common")

FILE(GLOB dramsim2_SOURCE *.cpp)
FILE(GLOB dramsim2_HEADER *.h)

SOURCE_GROUP("Source Files" FILES ${dramsim2_SOURCE})
SOURCE_GROUP("Header Files" FILES ${dramsim2_HEADER})

SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -D_SIM_")

##################################
# Add library

ADD_LIBRARY(dramsim2 ${dramsim2_SOURCE} ${dramsim2_HEADER})