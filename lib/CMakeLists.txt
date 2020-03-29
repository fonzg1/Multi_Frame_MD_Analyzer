# /library/CMakeLists.txt

add_library( basicmath_ObjLib  OBJECT  "src/dummy.cpp" )

# Required include search-paths and constexpr support.
target_include_directories( basicmath_ObjLib
  PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include"
  )

target_compile_features( basicmath_ObjLib
  PUBLIC cxx_constexpr
  )

# requires "" (which has some requirements, too).
target_link_libraries( basicmath_ObjLib PUBLIC   )
