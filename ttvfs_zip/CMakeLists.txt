
set(ttvfs_zip_SRC
    VFSDirZip.cpp
    VFSFileZip.cpp
    VFSZipArchiveLoader.cpp
    VFSZipArchiveRef.cpp
    miniz.c
    miniz.h
)

set(ttvfs_zip_HEADERS
    VFSDirZip.h
    VFSFileZip.h
    VFSZipArchiveLoader.h
    VFSZipArchiveRef.h
    ttvfs_zip.h
)

include_directories(${TTVFS_INCLUDE_DIRS})

add_library(ttvfs_zip ${ttvfs_zip_SRC} ${ttvfs_zip_HEADERS})

install(TARGETS ttvfs_zip DESTINATION lib${LIB_SUFFIX})
install(FILES ${ttvfs_zip_HEADERS} DESTINATION include/ttvfs_zip)
