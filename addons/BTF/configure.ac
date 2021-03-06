AC_INIT([btf], [1.2.4], [davis@cise.ufl.edu])

AC_CONFIG_SRCDIR([Source/btf_order.c])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_AUX_DIR([config])

AM_INIT_AUTOMAKE([no-dist-gzip dist-bzip2 foreign])

# use silent rules if available - automake 1.11
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES(yes)])

LT_INIT
AC_PROG_CC

# Checks for typedefs, structures, and compiler characteristics
AC_FUNC_ERROR_AT_LINE

# Checks for required SuiteSparse libraries
AX_CHECK_PKG_LIB(
	[suitesparseconfig],
	[SuiteSparse_config.h],
	[SuiteSparse_malloc],,
	[AC_MSG_ERROR([Could not find suitesparseconfig library])])

AC_MSG_CHECKING([if libtool needs -no-undefined flag to build shared libraries])
case "${host}" in
  *-*-cygwin* | *-*-mingw*)
    ## Add in the -no-undefined flag to LDFLAGS for libtool.
    AC_MSG_RESULT([yes])
    NOUNDEFINED=" -no-undefined"
    ;;
  *)
    ## Don't add in anything.
    AC_MSG_RESULT([no])
    ;;
esac

AC_SUBST([NOUNDEFINED])

AC_CONFIG_FILES([Doc/Makefile
                 Source/Makefile
                 btf.pc
                 Makefile])
AC_OUTPUT
