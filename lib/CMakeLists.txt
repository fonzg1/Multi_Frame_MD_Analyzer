# /lib/CMakeLists.txt

add_library(ESBTL INTERFACE)

# Required include search-paths and constexpr support.
target_include_directories( ESBTL
  PUBLIC
  $<INSTALL_INTERFACE:include/ESBTL>
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include/ESBTL>
  PRIVATE
      ${CMAKE_CURRENT_SOURCE_DIR}/include/ESBTL/internal
      ${CMAKE_CURRENT_SOURCE_DIR}/include/ESBTL/properties
  )

target_compile_features(
  ESBTL
  INTERFACE cxx_std_11
  )


