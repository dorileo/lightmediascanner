MAINTAINERCLEANFILES = Makefile.in

AM_CPPFLAGS = -include $(top_builddir)/config.h \
		-I$(top_srcdir)/src/lib @SQLITE3_CFLAGS@
AM_CFLAGS = $(WARNINGFLAGS)
AM_LDFLAGS = $(GCLDFLAGS)

include_HEADERS = \
	lightmediascanner.h \
	lightmediascanner_plugin.h \
	lightmediascanner_utils.h \
	lightmediascanner_db.h \
	lightmediascanner_charset_conv.h
noinst_HEADERS = lightmediascanner_private.h lightmediascanner_db_private.h lightmediascanner_dlna.h

lib_LTLIBRARIES = liblightmediascanner.la

liblightmediascanner_la_SOURCES = \
	lightmediascanner.c \
	lightmediascanner_utils.c \
	lightmediascanner_charset_conv.c \
	lightmediascanner_process.c \
	lightmediascanner_check.c \
	lightmediascanner_db_common.c \
	lightmediascanner_db_image.c \
	lightmediascanner_db_audio.c \
	lightmediascanner_db_video.c \
	lightmediascanner_db_playlist.c \
	lightmediascanner_dlna_rules.c \
	lightmediascanner_dlna.c

liblightmediascanner_la_LIBADD = -ldl @SQLITE3_LIBS@ @LTLIBICONV@
liblightmediascanner_la_LDFLAGS = -version-info @version_info@
