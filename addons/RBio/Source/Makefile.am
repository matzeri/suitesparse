AM_CPPFLAGS = -I$(top_srcdir)/Include @SUITESPARSECONFIG_CFLAGS@

lib_LTLIBRARIES = librbio.la
librbio_la_SOURCES = RBio.c $(top_srcdir)/Include/RBio.h
librbio_la_LIBADD = @SUITESPARSECONFIG_LIBS@
librbio_la_LDFLAGS = -version-info 1:0:0 $(NOUNDEFINED)

MAINTAINERCLEANFILES = Makefile.in
