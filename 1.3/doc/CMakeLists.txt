##############################################################################
# @file  CMakeLists.txt
# @brief Build configuration of software documentation.
#
# This build configuration builds and/or installs the documentation of the
# software package. The documentation can be divided into user documentation
# (user manual) and developer documentation (developer manual). For
# developers, the documentation of the API is of particular interest,
# where developers who are responsible for maintaining the software
# may be provided with even more detailed documentation of the implementation.
#
# Copyright (c) <year> University of Pennsylvania. All rights reserved.<br />
# See http://www.rad.upenn.edu/sbia/software/license.html or COPYING file.
#
# Contact: SBIA Group <sbia-software at uphs.upenn.edu>
##############################################################################

# ============================================================================
# API documentation
# ============================================================================

# The following CMake code adds an API documentation to the 'doc' target which
# is automatically generated by Doxygen from the in-source code comments.
# Please refer to the documentation of basis_add_doc() for details.
#
# See basis_add_doc()

basis_add_doc (api GENERATOR Doxygen)

# ============================================================================
# manuals
# ============================================================================

# Add documentation files in the current directory and/or install these files
# using the macro basis_add_doc().
#
# See basis_add_doc()

if (EXISTS UserManual.pdf)
  basis_add_doc (UserManual.pdf OUTPUT_NAME "${PROJECT_NAME} User Manual.pdf")
endif ()
