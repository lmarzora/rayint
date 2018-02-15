file(GLOB HEADERS "*.h")
file(GLOB SOURCES "*.cpp")

set(BIN raycast)

add_executable(${BIN} ${SOURCES})
#add_dependencies(${BIN} mve)
#target_link_libraries(${BIN} -lmve -lmve_util ${JPEG_LIBRARIES} ${PNG_LIBRARIES} ${TIFF_LIBRARIES})
target_link_libraries(${BIN} ${MVE} ${MVE_UTIL_LIB} ${JPEG_LIBRARIES} ${PNG_LIBRARIES} ${TIFF_LIBRARIES})
target_include_directories(${BIN} SYSTEM PUBLIC ${MVE_INCLUDE_PATH})