cmake_minimum_required(VERSION 3.20)

set(simde_VERSION 0.7.2)

project(cmeel-simde VERSION ${simde_VERSION})

include(FetchContent)
FetchContent_Declare(simde
    URL "https://github.com/simd-everywhere/simde/archive/refs/tags/v${simde_VERSION}.tar.gz"
    URL_HASH SHA1=81e248cf45b38d2bbb8506d78803b569fb3c33bb
    DOWNLOAD_EXTRACT_TIMESTAMP OFF
    CONFIGURE_COMMAND ""
    BUILD_COMMAND ""
    INSTALL_COMMAND ""
    )
FetchContent_MakeAvailable(simde)
install(DIRECTORY "${simde_SOURCE_DIR}/simde" DESTINATION include)
