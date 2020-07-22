AM_CPPFLAGS = -I@top_srcdir@ -DEMBEDDED

AM_CFLAGS = \
    @LIBEVENT_CFLAGS@ \
    @LIBCURL_CFLAGS@ \
    @SYSTEMD_CFLAGS@ \
    @ZLIB_CFLAGS@ \
    @PTHREAD_CFLAGS@

EXTRA_DIST = \
    transmission-daemon.service

bin_PROGRAMS = \
    transmission-daemon

LDADD = \
    $(top_builddir)/libtransmission/libtransmission.a \
    @LIBUPNP_LIBS@ \
    @LIBNATPMP_LIBS@ \
    @DHT_LIBS@ \
    @LIBB64_LIBS@ \
    @LIBUTP_LIBS@ \
    @LIBEVENT_LIBS@ \
    @LIBCURL_LIBS@ \
    @CRYPTO_LIBS@ \
    @INTLLIBS@ \
    @SYSTEMD_LIBS@ \
    @ZLIB_LIBS@ \
    @PTHREAD_LIBS@ \
    ${LIBM}

noinst_HEADERS = daemon.h

transmission_daemon_SOURCES = daemon.c
transmission_daemon_SOURCES += daemon-posix.c
