cmake_minimum_required(VERSION 3.20)

set(NAME simde)
set(VERSION 0.7.6)

project("cmeel-${NAME}" VERSION ${VERSION})

include(FetchContent)
FetchContent_Declare(
  ${NAME}
  URL "https://github.com/simd-everywhere/${NAME}/archive/refs/tags/v${VERSION}.tar.gz"
  URL_HASH "SHA1=c24aa2d6581096583eebc8434668e75ca05d0262"
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
