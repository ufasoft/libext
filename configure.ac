AC_INIT(libext, 18.0, support@ufasoft.com,, http://github.com/ufasoft/el)
AC_CONFIG_MACRO_DIR([m4])
m4_include([m4/common.m4])


LT_PREREQ([2.4])
LT_INIT([disable-shared])


AC_CONFIG_SRCDIR([el/libext.h])


AS_IF([test "x$CLANG" = "xyes"],
    [AC_COMPILE_IFELSE([AC_LANG_SOURCE[
      #include <type_traits>
      #if !_LIBCPP_VERSION
      #error No libc++
      #endif
      void func() {}]
        ],                          [CLANG_LIBCPP=yes],
        [AC_MSG_ERROR([libc++ required for CLang++])]
        )
    ])

AC_CHECK_HEADERS([sys/time.h])

AC_CHECK_HEADER([filesystem], $have_filesystem=true)
AM_CONDITIONAL([HAVE_FILESYSTEM], [test x$have_filesystem = xtrue])

AC_CHECK_LIB(gmp, __gmpz_init, , [AC_MSG_ERROR([Missing required libgmp-dev])])

PKG_CHECK_MODULES([JANSSON], [jansson >= 2.0], AC_DEFINE([HAVE_JANSSON], [1], [Defined to 1 if Jansson is present on the system]), [AC_MSG_ERROR([Missing required libjansson-dev / jansson-devel >= 2.0])])
AC_SUBST(JANSSON_CFLAGS)
AC_SUBST(JANSSON_LIBS)

AC_CHECK_FUNCS([gettid])

AC_OUTPUT(Makefile)

AU_PRINT_SETTINGS





