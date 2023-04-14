cmake_minimum_required(VERSION 3.24)
project(cmakecm-composition LANGUAGES C)

include(FetchContent)

FetchContent_Declare(
        cmakecm-lib
        GIT_REPOSITORY https://github.com/oallaire/cmakecm-lib.git
        GIT_TAG        46d4ff8c80aaa50e323089dc035b6a4c3b65ae92
)
FetchContent_MakeAvailable(cmakecm-lib)

FetchContent_Declare(
        cmakecm-app1
        GIT_REPOSITORY https://github.com/oallaire/cmakecm-app1.git
        GIT_TAG        efa1d65d8e32fb7c7b2cf7c9c7ffa1b14b66b2f6
)
FetchContent_MakeAvailable(cmakecm-app1)

FetchContent_Declare(
        cmakecm-app2
        GIT_REPOSITORY https://github.com/oallaire/cmakecm-app2.git
        GIT_TAG        e800447f73ceb912ede8dbdee97af896f7830e8a
)
FetchContent_MakeAvailable(cmakecm-app2)

include(InstallRequiredSystemLibraries)
set(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_CURRENT_SOURCE_DIR}/LICENSE")
set(CPACK_PACKAGE_VERSION_MAJOR "0")
set(CPACK_PACKAGE_VERSION_MINOR "1")
set(CPACK_SOURCE_GENERATOR "TGZ")
include(CPack)
