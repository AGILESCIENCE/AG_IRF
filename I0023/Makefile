#############################################################################
# Makefile for building: AGILE ASDC software GRID SCI
# Last modification: 2008-06-03  (Andrea Bulgarelli)
# Project:  AGILE ASDC
# Template: system
# Use make variable_name=' options ' to override the variables or make -e to
# override the file variables with the environment variables
# 		make CFLAGS='-g' or make prefix='/usr'
# Instructions:
# - if you want, modify the sections 1) and 2) but it is not necessary
# - modify the variables of the section 3): CFLAGS
# - in section 4), modify the following action:
#		* checkout: modify the project and option -r
#			cvs checkout -r TAG_NAME prj_name
#		* all: and or remove exe and lib prerequisite
#		* clean: add or remove the files and directories that should be cleaned
#		* install: add or remove the files and directories that should be installed
#		* uninstall: add or remove the files and directories that should be uninstalled
#############################################################################

SHELL = /bin/sh

####### 0) Common definition
# DISCOS Type is the different type of DISCoS operating mode
# EGSE_DISCOS is for the DISCoS at EGSE level
DISCOS_TYPE = EGSE_DISCOS
# EGSE_TE is for the DISCoS at TE level
#DISCOS_TYPE = TE_DISCOS
####### 1) Directories for the installation

# Prefix for each installed program. Only ABSOLUTE PATH
prefix=$(HOME)/ADC
exec_prefix=$(prefix)
# The directory to install the binary files in.
bindir=$(exec_prefix)/bin
# The directory to install the local configuration file.
datadir=$(exec_prefix)/share
# The directory to install the libraries in.
libdir=$(exec_prefix)/lib
# The directory to install the info files in.
infodir=$(exec_prefix)/info
# The directory to install the include files in.
includedir=$(exec_prefix)/include

####### 2) Directories
PRJ_DIR=Projects

INSTALL_SUBDIR=


####### 3) Compiler, tools and options

#Insert the optional parameter to the compiler. The CFLAGS could be changed externally by the user
CFLAGS   =
AR       = ar cqs
TAR      = tar -cf
GZIP     = gzip -9f
COPY     = cp -f
COPY_FILE= $(COPY) -p
COPY_DIR = $(COPY) -pR
DEL_FILE = rm -f
SYMLINK  = ln -sf
DEL_DIR  = rm -rf
MOVE     = mv -f
CHK_DIR_EXISTS= test -d
MKDIR    = mkdir -p
CVS = cvs -d${CVSROOT} checkout

BUILD = -r BUILD18_SCI
#BUILD =

####### 4) Build rules
all:
	test -d $(exec_prefix)/scientific_analysis/data/ || $(MKDIR) $(exec_prefix)/scientific_analysis/data/
	$(COPY_DIR) ./* $(exec_prefix)/scientific_analysis/data/

install: all

