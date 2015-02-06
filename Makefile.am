AM_CPPFLAGS = -I$(top_srcdir)

libext_FILES = 						\
	el/libext/file_config.h             \
	el/libext/afterstl.h			\
	el/libext/c-old.h				\
	el/libext/cpp-old.h				\
	el/libext/ext-cpu.h				\
	el/libext/ext-regex.h			\
	el/libext/ext-hash.h			\
	el/libext/ext-http.h			\
	el/libext/ext-lru.h				\
	el/libext/ext-macro.h			\
	el/libext/ext-meta.h			\
	el/libext/ext-protocols.h		\
	el/libext/ext-str.h				\
	el/libext/ext-ptr.h				\
	el/libext/facilities.h			\
	el/libext/gcc-intrinsic.h		\
	el/libext/ext-protocols.cpp		\
	el/libext/ext-ip-address.cpp	\
	el/libext/ext-net.cpp			\
	el/libext/mapped-file.cpp		\
	el/libext/varvalue.cpp			\
	el/libext/ext-json.cpp			\
	el/libext/http.cpp				\
	el/libext/ext-posix-win.h		\
	el/libext/vc.h					\
	el/vc/vc-warnings.h				\
	el/libext/bignum.cpp			\
	el/comp/mean.h					\
	el/bignum.h						\
	el/inet/async-text-client.h		\
	el/inet/async-text-client.cpp	\
	el/inet/json-rpc.h				\
	el/inet/json-rpc.cpp			\
    el/inet/detect-global-ip.cpp	\
    el/inet/p2p-net.cpp				\
    el/inet/p2p-peers.cpp			\
    el/inet/p2p-net.h				\
    el/inet/p2p-peers.h             \
    el/inet/detect-global-ip.h 		\
	el/num/mod.h					\
	el/num/mod.cpp					\
	el/num/num.h					\
	el/num/num.cpp					\
	el/num/prime.h					\
	el/num/prime.cpp				\
	el/stl/codecvt					\
	el/stl/codecvt.cpp				\
	el/stl/filesystem				\
	el/stl/filesystem.cpp				

lib_LTLIBRARIES = libext.la 

libext_la_SOURCES = 				\
	el/libext/binary-reader-writer.cpp	\
	el/libext/datetime.cpp			\
	el/libext/ext-app.cpp			\
	el/libext/ext-base.cpp			\
	el/libext/ext-blob.cpp			\
	el/libext/ext-core.cpp			\
	el/libext/ext-encoding.cpp		\
	el/libext/ext-file.cpp			\
	el/libext/ext-fw.cpp			\
	el/libext/ext-handlers.cpp		\
	el/libext/ext-os.cpp			\
	el/libext/ext-stream.cpp		\
	el/libext/ext-string.cpp		\
	el/libext/ext-sync.h			\
	el/libext/ext-blob.h			\
	el/libext/ext-safehandle.h		\
	el/libext/murmurhash.cpp 		\
	el/libext/sockets.cpp 			\
	el/libext/stack-trace.cpp		\
	el/libext/threader.cpp			\
	el/libext/exthelpers.h			\
	el/libext/libext.vcxproj		\
	el/libext/libext.vcxproj.filters

nobase_include_HEADERS = 			\
	el/libext.h						\
	el/ext_messages.h				\
	el/inc/default-defs.h			\
	el/inc/ext_config.h				\
	el/inc/inc_configs.h			\
	el/libext/binary-reader-writer.h	\
	el/libext/datetime.h			\
	el/libext/interlocked.h			\
	el/libext/ext-app.h				\
	el/libext/ext-base.h			\
	el/libext/ext-cpp.h				\
	el/libext/ext-core.h			\
	el/libext/ext-fw.h				\
	el/libext/ext-os.h				\
	el/libext/ext-net.h				\
	el/libext/ext-stream.h			\
	el/libext/ext-string.h			\
	el/libext/ext-thread.h			

if HAVE_FILESYSTEM
else
libext_la_SOURCES += el/stl/filesystem.cpp
nobase_include_HEADERS += el/stl/filesystem
endif


uninstall-hook:
	if test -d ${includedir}/el; then rmdir ${includedir}/el/libext ${includedir}/el/inc ${includedir}/el; fi




