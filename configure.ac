AC_INIT(libext, 7.0, support@ufasoft.com,, http://github.com/ufasoft/el)
m4_include([m4/common.m4])


LT_PREREQ([2.4])
LT_INIT([disable-shared])


AC_CONFIG_SRCDIR([el/libext.h])

AC_PROG_CC([clang gcc])
AC_PROG_CXX([clang++ g++])
AM_PROG_CC_C_O
AC_LANG([C++])

AX_CHECK_COMPILE_FLAG([-std=c++1y], [CXXFLAGS="$CXXFLAGS -std=c++1y"], [CXXFLAGS="$CXXFLAGS -std=c++0x"])


AC_COMPILE_IFELSE([AC_LANG_PROGRAM([], [[
	#ifndef __clang__
		not clang
	#endif
	]])],
	[CLANG=yes], [CLANG=no])

if test "x$CLANG" = "xyes"; then
	CXXFLAGS="$CXXFLAGS -stdlib=libc++"
fi

AS_IF([test "x$CLANG" = "xyes"], 
	[AC_COMPILE_IFELSE([AC_LANG_SOURCE[
	  #include <type_traits> 
	  #if !_LIBCPP_VERSION  
	  #error No libc++      
	  #endif                
	  void func() {}]       
		],                       	[CLANG_LIBCPP=yes], 
		[AC_MSG_ERROR([libc++ required fo CLang++])]
		)
	])

AC_CHECK_HEADER([filesystem], $have_filesystem=true)
AM_CONDITIONAL([HAVE_FILESYSTEM], [test x$have_filesystem = xtrue])
AC_CHECK_LIB(gmp, __gmpz_init, , [AC_MSG_ERROR([Missing required libgmp-dev])])

PKG_CHECK_MODULES([JANSSON], [jansson >= 2.0], AC_DEFINE([HAVE_JANSSON], [1], [Defined to 1 if Jansson is present on the system]), [AC_MSG_ERROR([Missing required libjansson-dev / jansson-devel >= 2.0])])
AC_SUBST(JANSSON_CFLAGS)
AC_SUBST(JANSSON_LIBS)


AC_OUTPUT(Makefile)

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
echo "Compilation............: make (gmake on FreeBSD)"
echo "  CPPFLAGS.............: $CPPFLAGS"
echo "  CFLAGS...............: $CFLAGS"
echo "  CXXFLAGS.............. $CXXFLAGS"
echo
echo "Installation...........: make install (as root if needed, with 'su' or 'sudo')"
echo "  prefix...............: $prefix"
echo


HELLO_WORLD




