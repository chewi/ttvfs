
set(cfileapi_SRC
    ttvfs_stdio.cpp
    ttvfs_stdio.h
)

include_directories(${TTVFS_INCLUDE_DIRS})

add_library(ttvfs_cfileapi ${cfileapi_SRC})
set_target_properties(ttvfs_cfileapi PROPERTIES VERSION 0.0.1 SOVERSION 0)

target_link_libraries(ttvfs_cfileapi ttvfs)

install(TARGETS ttvfs_cfileapi DESTINATION lib${LIB_SUFFIX})
install(FILES ttvfs_stdio.h DESTINATION include/ttvfs_cfileapi)
