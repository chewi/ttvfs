
set(ttvfs_SRC
    VFSBase.cpp
    VFSDebug.cpp
    VFSDir.cpp
    VFSDirInternal.cpp
    VFSDirView.cpp
    VFSFile.cpp
    VFSFileFuncs.cpp
    VFSLoader.cpp
    VFSRoot.cpp
    VFSSystemPaths.cpp
    VFSTools.cpp
)

set(ttvfs_HEADERS
    ttvfs.h
    VFSArchiveLoader.h
    VFSBase.h
    VFSDebug.h
    VFSDefines.h
    VFSDir.h
    VFSDirInternal.h
    VFSDirView.h
    VFSFile.h
    VFSFileFuncs.h
    VFSInternal.h
    VFSLoader.h
    VFSRefcounted.h
    VFSRoot.h
    VFSSystemPaths.h
    VFSTools.h
)

add_library(ttvfs ${ttvfs_SRC} ${ttvfs_HEADERS})

install(TARGETS ttvfs DESTINATION lib${LIB_SUFFIX})
install(FILES ${ttvfs_HEADERS} DESTINATION include/ttvfs)
