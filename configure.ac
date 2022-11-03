# Process this file with autoconf to produce a configure script

AC_PREREQ(2.69)
AC_INIT([libpainter], [0.1.1], [xrdp-devel@googlegroups.com])
AC_CONFIG_HEADERS(config_ac.h:config_ac-h.in)
AM_INIT_AUTOMAKE([1.6 foreign])
AC_CONFIG_MACRO_DIR([m4])
AC_PROG_CC
AC_C_CONST
LT_INIT
PKG_INSTALLDIR

# Use silent rules by default if supported by Automake
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

AX_CFLAGS_WARN_ALL
AX_APPEND_COMPILE_FLAGS([-Wwrite-strings])

AC_ARG_ENABLE(tests, AS_HELP_STRING([--enable-tests],
              [Build install tests (default: no)]),
              [], [enable_tests=no])
AM_CONDITIONAL(PT_TESTS, [test x$enable_tests = xyes])

AC_CONFIG_FILES([
  Makefile
  include/Makefile
  pkgconfig/libpainter.pc
  pkgconfig/libpainter-uninstalled.pc
  pkgconfig/Makefile
  src/Makefile
  tests/Makefile
])

AC_OUTPUT
