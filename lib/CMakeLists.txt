# /lib/CMakeLists.txt

add_library(ESBTL INTERFACE)

# Required include search-paths and constexpr support.
target_include_directories( ESBTL
  INTERFACE
      $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include/ESBTL>
      $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include/ESBTL/internal>
      $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include/ESBTL/properties>
      $<INSTALL_INTERFACE:include/ESBTL>
      $<INSTALL_INTERFACE:include/ESBTL/internal>
      $<INSTALL_INTERFACE:include/ESBTL/properties>
  )

target_compile_features(
  ESBTL
  INTERFACE cxx_std_11
  )


