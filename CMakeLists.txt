cmake_minimum_required(FATAL_ERROR VERSION 3.12...3.17)

# Get version and description
include("${CMAKE_CURRENT_LIST_DIR}/cmake/project-meta-info.in")

project( Multi_Frame_MD_Analyzer
         VERSION 0.1.0
         DESCRIPTION "Multi-Model PDB MD simulation analyzer"
  )

# include this directory to access helper functions, macros, and other tools
add_subdirectory(cmake)

# Make external libraries globally available.
add_subdirectory(external)

# Create targets for building the (local) libraries.
add_subdirectory(lib)

# documentation directory
add_subdirectory(doc)

# Create the targets for the entire app.
add_subdirectory(app)
