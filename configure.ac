AC_PREREQ([2.67])
AC_INIT(libext, 7.0, support@ufasoft.com,, http://github.com/ufasoft/el)
AC_CONFIG_MACRO_DIR([m4])

AM_INIT_AUTOMAKE([foreign subdir-objects dist-xz])
AM_SILENT_RULES([yes])

LT_PREREQ([2.4])
LT_INIT([disable-shared])


AC_CONFIG_SRCDIR([el/libext.h])

AC_PROG_CC([clang gcc])
AC_PROG_CXX([clang++ g++])
AM_PROG_CC_C_O
AC_LANG([C++])


AC_OUTPUT(Makefile)

echo
echo
echo
echo "------------------------------------------------------------------------"
echo "$PACKAGE $VERSION"
echo "------------------------------------------------------------------------"
echo
echo
echo "Configuration Options Summary:"
echo




echo
echo
echo "Compilation............: make (gmake on FreeBSD)"
echo "  CPPFLAGS.............: $CPPFLAGS"
echo "  CFLAGS...............: $CFLAGS"
echo "  CXXFLAGS.............. $CXXFLAGS"
echo
echo "Installation...........: make install (as root if needed, with 'su' or 'sudo')"
echo "  prefix...............: $prefix"
echo






