project(dramsim2)
INCLUDE("${esesc_SOURCE_DIR}/CMake.common")

FILE(GLOB dramsim2_SOURCE *.cpp)
FILE(GLOB dramsim2_HEADER *.h)

SOURCE_GROUP("Source Files" FILES ${dramsim2_SOURCE})
SOURCE_GROUP("Header Files" FILES ${dramsim2_HEADER})

##################################
# Add library

FILE(GLOB exec_SOURCE1 TraceBasedSim.cpp)

LIST(REMOVE_ITEM dramsim2_SOURCE exec_SOURCE1)

ADD_LIBRARY(dramsim2 ${dramsim2_SOURCE} ${dramsim2_HEADER})