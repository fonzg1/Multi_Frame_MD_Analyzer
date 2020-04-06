cmake_minimum_required(FATAL_ERROR VERSION 3.12...3.17)

# Get version and description
include("${CMAKE_CURRENT_LIST_DIR}/cmake/project-meta-info.in")

project( Multi_Frame_MD_Analyzer
         DESCRIPTION "Multi-Model PDB MD simulation analyzer"
         LANGUAGES CXX
  )

###############################################################################
# Project wide setup

# include this directory to access helper functions, macros, and other tools
list(APPEND CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake")

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED YES)
set(CMAKE_CXX_EXTENSIONS NO)

###############################################################################

# Make external libraries globally available.
add_subdirectory(external)

###############################################################################


###############################################################################
# Main targets built by this project

# Create targets for building the (local) libraries.
add_subdirectory(lib)

# Create the targets for the entire app.
add_subdirectory(app)
###############################################################################
