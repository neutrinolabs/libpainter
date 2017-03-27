EXTRA_DIST =

EXTRA_INCLUDES =
EXTRA_LIBS =
EXTRA_FLAGS =

AM_CPPFLAGS = \
  -I$(top_srcdir)/include \
  $(EXTRA_INCLUDES)

bin_PROGRAMS = paintertest

paintertest_SOURCES = paintertest.c

paintertest_LDADD = \
  $(top_builddir)/src/libpainter.la $(EXTRA_LIBS)

paintertest_LDFLAGS = $(EXTRA_FLAGS)

