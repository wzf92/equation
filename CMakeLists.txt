PROJECT(main)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

ADD_SUBDIRECTORY(gui)
ADD_SUBDIRECTORY(core)
find_package(Qt4 REQUIRED)
INCLUDE(${QT_USE_FILE})

AUX_SOURCE_DIRECTORY(. DIR_SRCS)

ADD_EXECUTABLE(main ${DIR_SRCS})
TARGET_LINK_LIBRARIES(main GUI CORE)
