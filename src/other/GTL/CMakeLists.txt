# Minimum required version of CMake
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
IF(COMMAND CMAKE_POLICY)
	CMAKE_POLICY(SET CMP0003 NEW)
ENDIF(COMMAND CMAKE_POLICY)

# set CMake project name
PROJECT(GTL)

SET(GTL_MAJOR_VERSION 1)
SET(GTL_MINOR_VERSION 2)
SET(GTL_PATCH_VERSION 4)
SET(GTL_VERSION ${GTL_MAJOR_VERSION}.${GTL_MINOR_VERSION}.${GTL_PATCH_VERSION})

# shared library versioning
#
# current:revision:age
#    |        |     |
#    |        |     +- increment if interfaces have been added
#    |        |        set to zero if interfaces have been removed
#                      or changed
#    |        +- increment if source code has changed
#    |           set to zero if current is incremented
#    +- increment if interfaces have been added, removed or changed

SET(GTL_LIB_CURRENT 3)
SET(GTL_LIB_REVISION 4)
SET(GTL_LIB_AGE 2)
SET(GTL_SO_VERSION ${GTL_LIB_CURRENT}.${GTL_LIB_REVISION}.${GTL_LIB_AGE})

ADD_SUBDIRECTORY(src)
ADD_SUBDIRECTORY(include)
#ADD_SUBDIRECTORY(doc)
#ADD_SUBDIRECTORY(tests)
