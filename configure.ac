#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.64])
AC_INIT(c_template, 0.1, quanyangyi0323@gmail.com)
AC_CONFIG_SRCDIR([include/doxygen_mainpage.h])
AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE

AC_ARG_ENABLE(debug,
[  --enable-debug          turn on debugging],
[case "${enableval}" in
  yes) debug=true ;;
  no)  debug=false ;;
  *) AC_MSG_ERROR(bad value ${enableval} for --enable-debug) ;;
esac],[debug=false])
AM_CONDITIONAL(DEBUG, test x$debug = xtrue)

AC_ARG_ENABLE(profile,
[  --enable-profile        turn on profiling],
[case "${enableval}" in
  yes) profile=true ;;
  no)  profile=false ;;
  *) AC_MSG_ERROR(bad value ${enableval} for --enable-profile) ;;
esac],[profile=false])
AM_CONDITIONAL(PROFILE, test x$profile = xtrue)

AC_ARG_ENABLE(coverage,
[  --enable-coverage       turn on coverage feature],
[case "${enableval}" in
  yes) coverage=true ;;
  no)  coverage=false ;;
  *) AC_MSG_ERROR(bad value ${enableval} for --enable-coverage) ;;
esac],[coverage=false])
AM_CONDITIONAL(COVERAGE, test x$coverage = xtrue)

# Checks for programs.
AC_PROG_CC

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_CONFIG_FILES([Makefile
                 include/Makefile
                 src/Makefile
                 spec/Makefile])
AC_OUTPUT
