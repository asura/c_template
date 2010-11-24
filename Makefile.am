SUBDIRS = include src spec

doc: Doxyfile
	cd $(top_srcdir); doxygen Doxyfile

if COVERAGE
gcov:	FORCE
	cd src; gcov -b -f *.gcda
	cd spec; gcov -b -f *.gcda
	lcov -c -d . -o lcov.info
	genhtml -o gcov lcov.info
	gcovr.py -b -x > coverage.xml
endif

splint.log: FORCE
	splint -I$(top_srcdir)/include $(top_srcdir)/src/*.c > $@

.cccc: FORCE
	cccc ../src/*.c ../spec/*.c

FORCE:
