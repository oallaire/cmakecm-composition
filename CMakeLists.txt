cmake_minimum_required(VERSION 3.22)
project(cmakecm-composition LANGUAGES C)

include(FetchContent)

FetchContent_Declare(
        cmakecm-lib
        GIT_REPOSITORY https://github.com/oallaire/cmakecm-lib.git
        GIT_TAG        e026562b7f8cc3e24a05d1aaf01f5a29f2329df0
)
FetchContent_MakeAvailable(cmakecm-lib)

FetchContent_Declare(
        cmakecm-app1
        GIT_REPOSITORY https://github.com/oallaire/cmakecm-app1.git
        GIT_TAG        18857c5381801b2acf278f651c226d3a781e4c1d
)
FetchContent_MakeAvailable(cmakecm-app1)

FetchContent_Declare(
        cmakecm-app2
        GIT_REPOSITORY https://github.com/oallaire/cmakecm-app2.git
        GIT_TAG        e38abcc65eefdea996ec379b6396c749cd70c7d5
)
FetchContent_MakeAvailable(cmakecm-app2)

include(InstallRequiredSystemLibraries)
set(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_CURRENT_SOURCE_DIR}/LICENSE")
set(CPACK_PACKAGE_VERSION_MAJOR "0")
set(CPACK_PACKAGE_VERSION_MINOR "1")
set(CPACK_SOURCE_GENERATOR "TGZ")
include(CPack)
