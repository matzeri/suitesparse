AM_CPPFLAGS = -I$(top_srcdir)/Include @SUITESPARSECONFIG_CFLAGS@

lib_LTLIBRARIES = libcolamd.la
noinst_LTLIBRARIES = libcolamdi.la libcolamdl.la

libcolamdl_la_SOURCES = colamd.c $(top_srcdir)/Include/colamd.h
libcolamdl_la_CPPFLAGS = $(AM_CPPFLAGS) -DDLONG

libcolamdi_la_SOURCES = $(libcolamdl_la_SOURCES)

libcolamd_la_SOURCES = 
libcolamd_la_LIBADD = libcolamdi.la libcolamdl.la @SUITESPARSECONFIG_LIBS@
libcolamd_la_LDFLAGS = -version-info 1:0:0 $(NOUNDEFINED)

MAINTAINERCLEANFILES = Makefile.in
