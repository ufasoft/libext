ACLOCAL_AMFLAGS = -I m4
AM_CPPFLAGS = -I$(top_srcdir)

lib_LTLIBRARIES = libext.la 

libext_la_SOURCES = 				\
	el/libext/binary-reader-writer.cpp	\
	el/libext/bignum.cpp			\
	el/libext/datetime.cpp			\
	el/libext/ext-app.cpp			\
	el/libext/ext-base.cpp			\
	el/libext/ext-blob.cpp			\
	el/libext/ext-core.cpp			\
	el/libext/ext-encoding.cpp		\
	el/libext/ext-file.cpp			\
	el/libext/ext-fw.cpp			\
	el/libext/ext-handlers.cpp		\
	el/libext/ext-ip-address.cpp	\
	el/libext/ext-json.cpp			\
	el/libext/ext-net.cpp			\
	el/libext/ext-os.cpp			\
	el/libext/ext-protocols.cpp		\
	el/libext/ext-stream.cpp		\
	el/libext/ext-string.cpp		\
	el/libext/http.cpp				\
	el/libext/murmurhash.cpp 		\
	el/libext/rt.cpp		 		\
	el/libext/sockets.cpp 			\
	el/libext/stack-trace.cpp		\
	el/libext/threader.cpp			\
	el/libext/varvalue.cpp			\
	el/libext/libext.vcxproj		\
	el/libext/libext.vcxproj.filters \
	el/stl/decimal.cpp 				\
	el/stl/dynamic_bitset.cpp

nobase_include_HEADERS = 			\
	el/ext.h						\
	el/bignum.h						\
	el/libext.h						\
	el/ext_messages.h				\
	el/inc/default-defs.h			\
	el/inc/ext_config.h				\
	el/inc/inc_configs.h			\
	el/inc/extver.h					\
	el/libext/afterstl.h			\
	el/libext/binary-reader-writer.h	\
	el/libext/c-old.h				\
	el/libext/cpp-old.h				\
	el/libext/datetime.h			\
	el/libext/facilities.h			\
	el/libext/gcc-intrinsic.h		\
	el/libext/interlocked.h			\
	el/libext/exthelpers.h			\
	el/libext/ext-app.h				\
	el/libext/ext-base.h			\
	el/libext/ext-blob.h			\
	el/libext/ext-cpp.h				\
	el/libext/ext-core.h			\
	el/libext/ext-cpu.h				\
	el/libext/ext-fw.h				\
	el/libext/ext-hash.h			\
	el/libext/ext-http.h			\
	el/libext/ext-lru.h				\
	el/libext/ext-macro.h			\
	el/libext/ext-meta.h			\
	el/libext/ext-net.h				\
	el/libext/ext-os.h				\
	el/libext/ext-posix-win.h		\
	el/libext/ext-protocols.h		\
	el/libext/ext-ptr.h				\
	el/libext/ext-regex.h			\
	el/libext/ext-safehandle.h		\
	el/libext/ext-str.h				\
	el/libext/ext-stream.h			\
	el/libext/ext-string.h			\
	el/libext/ext-sync.h			\
	el/libext/ext-thread.h			\
	el/stl/decimal 					\
	el/stl/dynamic_bitset

if !HAVE_FILESYSTEM
libext_la_SOURCES += el/stl/filesystem.cpp
nobase_include_HEADERS += el/stl/filesystem
endif

if !HAVE_CODECVT
libext_la_SOURCES += el/stl/codecvt.cpp
nobase_include_HEADERS += el/stl/codecvt
endif

if !HAVE_REGEX
libext_la_SOURCES += el/stl/regex.cpp
nobase_include_HEADERS += el/stl/regex
endif

src/el/stl/filesystem : src/el/stl/filesystem
	echo "---"


uninstall-hook:
	if test -d ${includedir}/el; then rmdir ${includedir}/el/libext ${includedir}/el/inc ${includedir}/el; fi




