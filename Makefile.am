ACLOCAL_AMFLAGS = -I m4

SUBDIRS = \
  third-party \
  libtransmission \
  utils \
  daemon

EXTRA_DIST = \
  NEWS.md \
  AUTHORS \
  COPYING \
  README.md \
  autogen.sh \
  update-version-h.sh

if HAVE_REVISION_FILE
  EXTRA_DIST += REVISION
endif

dist-hook:
	find "$(distdir)/qt" "$(distdir)/cmake" -name .svn -exec rm -rf '{}' '+' -prune

DISTCLEANFILES = \
  intltool-extract \
  intltool-merge \
  intltool-update
