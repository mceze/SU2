# SU2 Makefile.am for SU2_DOT
# SU2 v3.2.7 "eagle"
#
# SU2 Lead Developers: Dr. Francisco Palacios (Francisco.D.Palacios@boeing.com).
#                      Dr. Thomas D. Economon (economon@stanford.edu).
#
# SU2 Developers: Prof. Juan J. Alonso's group at Stanford University.
#                 Prof. Piero Colonna's group at Delft University of Technology.
#                 Prof. Nicolas R. Gauger's group at Kaiserslautern University of Technology.
#                 Prof. Alberto Guardone's group at Polytechnic University of Milan.
#                 Prof. Rafael Palacios' group at Imperial College London.
#
# Copyright (C) 2012-2015 SU2, the open-source CFD code.
#
# SU2 is free software; you can redistribute it and/or
# modify it under the terms of the GNU Lesser General Public
# License as published by the Free Software Foundation; either
# version 2.1 of the License, or (at your option) any later version.
#
# SU2 is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
# Lesser General Public License for more details.
#
# You should have received a copy of the GNU Lesser General Public
# License along with SU2. If not, see <http://www.gnu.org/licenses/>.
#
# Created: 		10/26/12
# Last updated: 	3/12/13
#
# Created by: 		M. Colonno
# Updated by: 		M. Colonno
#
######################################################################################

# AUTOMAKE_OPTIONS = subdir-objects
ACLOCAL_AMFLAGS = ${ACLOCAL_FLAGS}

bin_PROGRAMS = ../bin/SU2_DOT

___bin_SU2_DOT_SOURCES = ../include/SU2_DOT.hpp \
		../src/SU2_DOT.cpp

___bin_SU2_DOT_CXXFLAGS =
___bin_SU2_DOT_LDADD = ../../Common/lib/libSU2.a

# always link to built dependencies from ./externals
___bin_SU2_DOT_CXXFLAGS += @su2_externals_INCLUDES@
___bin_SU2_DOT_LDADD += @su2_externals_LIBS@

# if BUILD_CGNS
___bin_SU2_DOT_CXXFLAGS += @CGNS_CXX@
___bin_SU2_DOT_LDADD += @CGNS_LD@
# endif

# if BUILD_MUTATIONPP
___bin_SU2_DOT_CXXFLAGS += @MUTATIONPP_CXX@
___bin_SU2_DOT_LDADD += @MUTATIONPP_LD@
# endif

# if BUILD_JSONCPP
___bin_SU2_DOT_CXXFLAGS += @JSONCPP_CXX@
___bin_SU2_DOT_LDADD += @JSONCPP_LD@
# endif
