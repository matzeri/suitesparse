AM_CPPFLAGS = -I$(top_srcdir)/Include @SUITESPARSECONFIG_CFLAGS@

AMDSRC = \
	$(top_srcdir)/Include/amd_internal.h \
	$(top_srcdir)/Include/amd.h \
	amd_1.c \
	amd_2.c \
	amd_aat.c \
	amd_control.c \
	amd_defaults.c \
	amd_dump.c \
	amd_info.c \
	amd_order.c \
	amd_postorder.c \
	amd_post_tree.c \
	amd_preprocess.c \
	amd_valid.c

noinst_LTLIBRARIES = libamdi.la libamdl.la
libamdi_la_SOURCES = $(AMDSRC)
libamdi_la_CPPFLAGS = $(AM_CPPFLAGS) -DDINT
libamdl_la_SOURCES = $(AMDSRC)
libamdl_la_CPPFLAGS = $(AM_CPPFLAGS) -DDLONG

lib_LTLIBRARIES = libamd.la
libamd_la_SOURCES = amd_global.c
libamd_la_LIBADD = libamdl.la libamdi.la @SUITESPARSECONFIG_LIBS@
libamd_la_LDFLAGS = -version-info 1:0:0 $(NOUNDEFINED)

if ENABLE_FORTRAN
lib_LTLIBRARIES += libamdf77.la
libamdf77_la_SOURCES = amd.f amdbar.f
endif

MAINTAINERCLEANFILES = Makefile.in
