#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.68])
AC_INIT([libdisorder], [0.0.2])
AC_CONFIG_SRCDIR([src/disorder.c])
AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE([foreign])

# Checks for programs.
AC_PROG_CC_C99
AC_PROG_LIBTOOL

# Checks for libraries.

# Checks for header files.
AC_CHECK_HEADERS([stdlib.h string.h math.h])

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.
AC_SEARCH_LIBS([log2], [m],
		    [AC_DEFINE([HAVE_LOG2], [1],
				[Define to 1 if log2() is available, else 0])],
		    [AC_DEFINE([HAVE_LOG2], [0])])

# Optional features
AC_ARG_ENABLE([ropy],
	AS_HELP_STRING([--enable-ropy],
			[Enable ropy tool [default=yes]]))
AM_CONDITIONAL([ENABLE_ROPY], [test "x$enable_ropy" != "xno"])

AC_CONFIG_FILES([Makefile
                 src/Makefile
                 tool/Makefile])
AC_OUTPUT
