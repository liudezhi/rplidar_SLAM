SET (sampleName rplidar_test)
SET (PRJ_NAME "EXAMPLE_${sampleName}")

PROJECT(${PRJ_NAME})
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

SET(EXECUTABLE_OUTPUT_PATH ".")

FIND_PACKAGE(MRPT REQUIRED hwdrivers;obs;gui)

ADD_EXECUTABLE(${sampleName} test.cpp)

TARGET_LINK_LIBRARIES(${sampleName}
			${MRPT_LIBS}
		     )
