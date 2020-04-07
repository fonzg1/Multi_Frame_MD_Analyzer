
add_executable(PDB_Reader ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp)
target_compile_features(PDB_Reader PRIVATE cxx_std_11)

target_link_libraries(PDB_Reader
  PRIVATE
      ESBTL
  )

