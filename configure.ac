AC_INIT(pSync, 0.8)
AM_INIT_AUTOMAKE

AC_SUBST(PACKAGE)
AC_SUBST(PACKAGE_VERSION)
AC_SUBST(prefix)

dnl Checks for programs.
AC_PROG_SED

dnl check for rsync
AC_PATH_PROG(RSYNC, [rsync],,[$PATH:$bindir:$prefix/bin])
if test -z "$RSYNC"; then echo "configure: error: ***rsync not found in PATH"; exit 1; fi

dnl check for get_config
AC_PATH_PROG(GET_CONFIG, [get_config],,[$PATH:$bindir:$prefix/bin])
if test -z "$GET_CONFIG"; then echo "configure: error: ***get_config not found in PATH"; exit 1; fi

AC_OUTPUT([
 Makefile \
 scripts/Makefile \
 scripts/pSync.sh
])

dnl *****************
dnl Configure summary
dnl *****************

echo
echo "$PACKAGE_NAME configuration:"
echo
echo "  Version      : $PACKAGE_VERSION"
echo "  Executables  : $prefix/bin/"
echo "  Configuration: defaults to $HOME/.pSync.conf"
echo
echo "Found tools and programs:"
echo "  sed 	    : $SED"
echo "  rsync	    : $RSYNC"
echo "  get_config: $GET_CONFIG"
echo
echo "Please see $PWD/doc/example_pSync.conf for a example"
echo "configuration file"
echo


