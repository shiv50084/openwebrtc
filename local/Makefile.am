## Process this file with automake to produce Makefile.in

AM_CPPFLAGS = \
    -DPACKAGE_LOCALE_DIR=\""$(localedir)"\" \
    -DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
    -DPACKAGE_DATA_DIR=\""$(pkgdatadir)"\" \
    $(GLIB_CFLAGS) \
    $(GSTREAMER_CFLAGS) \
    -I$(top_srcdir)/owr

AM_CFLAGS = \
    -ansi \
    -Wall \
    -Wextra \
    -Werror \
    -pedantic

noinst_LTLIBRARIES = libopenwebrtc_local.la

libopenwebrtc_local_la_SOURCES = \
    owr_local.c \
    owr_local_media_source.c \
    owr_media_renderer.c \
    owr_audio_renderer.c \
    owr_video_renderer.c \
    owr_image_renderer.c \
    owr_image_server.c

libopenwebrtc_local_la_LIBADD = \
    $(GSTREAMER_LIBS) \
    $(GLIB_LIBS)

includedir = $(prefix)/include/owr
include_HEADERS = \
    owr_local.h \
    owr_local_media_source.h \
    owr_media_renderer.h \
    owr_audio_renderer.h \
    owr_video_renderer.h \
    owr_image_renderer.h \
    owr_image_server.h

noinst_HEADERS = \
    owr_local_media_source_private.h \
    owr_media_renderer_private.h \
    owr_image_renderer_private.h

-include $(top_srcdir)/git.mk
