AM_CPPFLAGS = -I$(top_srcdir)/Include @SUITESPARSECONFIG_CFLAGS@

lib_LTLIBRARIES = libccolamd.la
noinst_LTLIBRARIES = libccolamdi.la libccolamdl.la

libccolamdl_la_SOURCES = ccolamd.c $(top_srcdir)/Include/ccolamd.h
libccolamdl_la_CPPFLAGS = $(AM_CPPFLAGS) -DDLONG

libccolamdi_la_SOURCES = $(libccolamdl_la_SOURCES)

libccolamd_la_SOURCES = 
libccolamd_la_LIBADD = libccolamdi.la libccolamdl.la @SUITESPARSECONFIG_LIBS@
libccolamd_la_LDFLAGS = -version-info 1:0:0 $(NOUNDEFINED)

MAINTAINERCLEANFILES = Makefile.in

