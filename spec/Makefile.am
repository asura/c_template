CFLAGS = -Wall

if DEBUG
CFLAGS += -g -DWITH_DMALLOC
LIBS += -ldmalloc
else
CFLAGS += -DNDEBUG -O2
endif

if PROFILE
CFLAGS += -pg
endif

if COVERAGE
CFLAGS += -fprofile-arcs -ftest-coverage
endif

INCLUDES = -I$(top_srcdir)/include -I$(includedir)

TESTS = spec
check_PROGRAMS = $(TESTS)
spec_SOURCES = spec_runner.c
spec_LDADD = -lcspec
