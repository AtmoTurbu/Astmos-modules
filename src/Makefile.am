#SUFFIXES = .c .h .y .l

bin_PROGRAMS = WOMAT
WOMAT_SOURCES = CLImain.c CommandLineInterface/CLIcore.c CommandLineInterface/CLIcore.h CommandLineInterface/calc_bison.y CommandLineInterface/calc_flex.l CommandLineInterface/calc.h
WOMAT_CPPFLAGS = -I@abs_top_srcdir@/src -DCONFIGDIR=\"@abs_top_srcdir@/config\" -DSOURCEDIR=\"@abs_top_srcdir@/src\" -DABSSRCTOPDIR=\"@abs_top_srcdir@\" -fopenmp -ldl

ACLOCAL_AMFLAGS = -I m4

## For Bison and FLEX
AM_YFLAGS = -d
AM_LFLAGS = -i 

## The contents of this variable are passed to every compilation that invokes the C preprocessor IF target_CPPFLAGS does not exit; it is a list of arguments to the preprocessor. For instance, -I and -D options should be listed here.
## AM_CPPFLAGS = -DCONFIGDIR=\"@abs_top_srcdir@/config\"

noinst_HEADERS = CommandLineInterface/calc.h

BUILT_SOURCES = CommandLineInterface/calc_bison.h


SUBDIRS = 
WOMAT_LDADD = 


## Modules are built as libraries of convenience
## Linking order matters

## 
## WOMAT modules : Wavefront Optics Material Atmospheric Turbulence
##

SUBDIRS += OpticsMaterials
WOMAT_LDADD += OpticsMaterials/libopticsmaterial.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/OpticsMaterials

SUBDIRS += WFpropagate
WOMAT_LDADD += WFpropagate/libwfpropagate.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/WFpropagate

SUBDIRS += AtmosphereModel
WOMAT_LDADD += AtmosphereModel/libatmospheremodel.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/AtmosphereModel

SUBDIRS += AtmosphericTurbulence
WOMAT_LDADD += AtmosphericTurbulence/libatmosphicturbulence.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/AtmosphericTurbulence


## Core modules last, higher level modules at the top

SUBDIRS += cudacomp
WOMAT_LDADD += cudacomp/libcudacomp.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/cudacomp

SUBDIRS += psf
WOMAT_LDADD += psf/libpsf.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/psf

SUBDIRS += img_reduce
WOMAT_LDADD += img_reduce/libimgreduce.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/img_reduce

SUBDIRS += image_format
WOMAT_LDADD += image_format/libimageformat.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/image_format

SUBDIRS += ZernikePolyn
WOMAT_LDADD += ZernikePolyn/libzernikepolyn.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/ZernikePolyn

SUBDIRS += image_basic
WOMAT_LDADD += image_basic/libimagebasic.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/image_basic

SUBDIRS += image_filter
WOMAT_LDADD += image_filter/libimagefilter.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/image_filter

SUBDIRS += image_gen
WOMAT_LDADD += image_gen/libimagegen.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/image_gen

SUBDIRS += linopt_imtools
WOMAT_LDADD += linopt_imtools/liblinoptimtools.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/linopt_imtools

SUBDIRS += statistic
WOMAT_LDADD += statistic/libstatistic.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/statistic

SUBDIRS += info
WOMAT_LDADD += info/libinfo.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/info

SUBDIRS += fft
WOMAT_LDADD += fft/libfft.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/fft


## 
## CORE modules, should always be included
##



SUBDIRS += COREMOD_arith
WOMAT_LDADD += COREMOD_arith/libcoremodarith.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_arith

SUBDIRS += COREMOD_memory
WOMAT_LDADD += COREMOD_memory/libcoremodmemory.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_memory

SUBDIRS += COREMOD_iofits
WOMAT_LDADD += COREMOD_iofits/libcoremodiofits.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_iofits

SUBDIRS += COREMOD_tools
WOMAT_LDADD += COREMOD_tools/libcoremodtools.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/COREMOD_tools

SUBDIRS += 00CORE
WOMAT_LDADD += 00CORE/lib00core.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/00CORE

SUBDIRS += ImageStreamIO
WOMAT_LDADD += ImageStreamIO/libimagestreamio.la
WOMAT_CPPFLAGS += -I@abs_top_srcdir@/src/ImageStreamIO
