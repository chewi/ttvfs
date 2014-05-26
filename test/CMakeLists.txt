
include_directories(${TTVFS_INCLUDE_DIRS})

add_executable(test1 test1.cpp)

target_link_libraries(test1 ttvfs)

enable_testing()
add_test(NAME test1 WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} COMMAND ${CMAKE_CURRENT_BINARY_DIR}/test1)
