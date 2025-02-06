cmake_minimum_required(VERSION 3.30)

set(ORG simd-everywhere)
set(NAME simde)
set(VERSION 0.8.2)
set(EXT tar.gz)
set(SHA256 ed2a3268658f2f2a9b5367628a85ccd4cf9516460ed8604eed369653d49b25fb)

project("cmeel-${NAME}" VERSION ${VERSION})

include(FetchContent)
FetchContent_Declare(
  ${NAME}
  URL "https://github.com/${ORG}/${NAME}/archive/refs/tags/v${VERSION}.${EXT}"
  URL_HASH "SHA256=${SHA256}"
  DOWNLOAD_EXTRACT_TIMESTAMP
  OFF
  CONFIGURE_COMMAND
  ""
  BUILD_COMMAND
  ""
  INSTALL_COMMAND
  "")
FetchContent_MakeAvailable(${NAME})
install(DIRECTORY "${${NAME}_SOURCE_DIR}/${NAME}" DESTINATION include)
