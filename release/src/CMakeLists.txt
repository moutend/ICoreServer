file(GLOB HEADERS "../include/ICoreServer/*.h")
source_group("Header Files\\CoreServer" FILES ${HEADERS})

file(GLOB SOURCES "./*.c")
list(APPEND SOURCES ${HEADERS})

add_library(ICoreServer ${SOURCES})
target_include_directories(ICoreServer PUBLIC $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include>)
