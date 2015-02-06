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

AX_CHECK_COMPILE_FLAG([-std=c++1y], [CXXFLAGS="$CXXFLAGS -std=c++1y"], [CXXFLAGS="$CXXFLAGS -std=c++0x"])


AC_COMPILE_IFELSE(
173    [AC_LANG_SOURCE[
174      #include <type_traits>
175      #if !_LIBCPP_VERSION
176      #error No libc++
177      #endif
178      void func() {}]
179    ],
180    [folly_cv_lib_libcpp=yes],
181    [folly_cv_lib_libcpp=no])


AC_COMPILE_IFELSE([AC_LANG_SOURCE[
  #include <type_traits> 
  #if !_LIBCPP_VERSION  
  #error No libc++      
  #endif                
  void func() {}]       
	],                       	[CLANG_LIBCPP=yes], [CLANG_LIBCPP=no])

if test "x$CLANG_LIBCPP" = "xyes"; then
	CXXFLAGS="$CXXFLAGS -stdlib=libc++"
fi

AC_CHECK_HEADER([filesystem], $have_filesystem=true)
AM_CONDITIONAL([HAVE_FILESYSTEM], [test x$have_filesystem = xtrue])


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






