#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ(2.69)
AC_INIT([xde-theme-blackbirds],[1.2.4],[https://github.com/bbidulock/xde-theme-blackbirds],[xde-theme-blackbirds],[https://github.com/bbidulock/xde-theme-blackbirds/issues])
AC_REVISION([1.2.4])

# set better defaults
AC_PREFIX_DEFAULT([/usr])
if test "$prefix" = /usr -o "$prefix" = NONE; then
	test "$sysconfdir" = '${prefix}/etc' && sysconfdir=/etc
	test "$sharedstatedir" = '${prefix}/com' && sharedstatedir=/var
	test "$localstatedir" = '${prefix}/var' && localstatedir=/var
fi

AC_CONFIG_SRCDIR([configure.ac])
AC_CONFIG_AUX_DIR([scripts])

DATE='2021-12-08'
AC_SUBST([DATE])

MDOCDATE='December 8, 2021'
AC_SUBST([MDOCDATE])

BRANCH='master'
AC_SUBST([BRANCH])

# Initialize Automake
AM_INIT_AUTOMAKE([1.16 dist-lzip no-dist-gzip std-options -Wall color-tests silent-rules tar-pax])
AM_MAINTAINER_MODE
AM_SILENT_RULES([yes])

# Checks for programs.
AC_PROG_SED
AC_PROG_AWK
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
AC_PROG_MKDIR_P

AC_ARG_VAR([MARKDOWN],[markdown command. @<:@default=markdown@:>@])
AC_CHECK_PROGS([MARKDOWN],[markdown],[${am_missing_run}markdown],[$PATH])

AC_ARG_VAR([ASCIIDOC],[asciidoc command. @<:@default=asciidoctor@:>@])
AC_CHECK_PROGS([ASCIIDOC],[asciidoc asciidoctor],[${am_missing_run}asciidoc],[$PATH])

AC_ARG_VAR([ASCIIDOC_BACKEND],[asciidoc backend @<:@default=NONE@:>@])
if test -z "$ASCIIDOC_BACKEND"; then
	case "$ASCIIDOC" in
		asciidoc) ASCIIDOC_BACKEND="--backend=html4" ;;
		asciidoctor) ASCIIDOC_BACKEND="--backend=html5" ;;
		*) AC_MSG_WARN([ASCIIDOC $ASCIIDOC is not supported.]) ;;
	esac
fi

AC_ARG_VAR([ASCIIMAN],[asciidoc to manpage converter. @<:@default=a2x@:>@])
AC_CHECK_PROGS([ASCIIMAN],[a2x asciidoctor],[${am_missing_run}a2x],[$PATH])

AC_ARG_VAR([ASCIIMAN_FORMAT],[asciidoc manpage option @<:@default=NONE@:>@])
if test -z "$ASCIIMAN_FORMAT"; then
	case "$ASCIIMAN" in
		a2x) ASCIIMAN_FORMAT="--format=manpage" ;;
		asciidoctor) ASCIIMAN_FORMAT="--backend=manpage" ;;
		*) AC_MSG_WARN([ASCIIMAN $ASCIIMAN is not supported.]) ;;
	esac
fi

AC_ARG_VAR([LINKS],[links command. @<:@default=lynx@:>@])
AC_CHECK_PROGS([LINKS],[lynx links],[${am_missing_run}lynx],[$PATH])
if test "$LINKS" = "links"; then
	LINKS="links -codepage utf-8"
fi

test "x$prefix" = xNONE && prefix="$ac_default_prefix"
sharedir="$datadir"
eval "sharedir=\"$sharedir\""
eval "sharedir=\"$sharedir\""
eval "sharedir=\"$sharedir\""
AC_SUBST([sharedir])

style='Blackbirds'
AC_SUBST([style])

stylesubdir='blackbirds'
AC_SUBST([stylesubdir])

basestyle='Squared-cadet'
AC_SUBST([basestyle])

baseprefix='sc'
AC_SUBST([baseprefix])

adwmdir='$(datadir)/adwm'
AC_SUBST([adwmdir])

adwmstylesdir='$(adwmdir)/styles'
AC_SUBST([adwmstylesdir])

adwmthemesdir='$(adwmdir)/themes'
AC_SUBST([adwmthemesdir])

adwmthemedir='$(adwmthemesdir)/$(style)'
AC_SUBST([adwmthemedir])

waimeadir='$(datadir)/waimea'
AC_SUBST([waimeadir])

waimeastylesdir='$(waimeadir)/styles'
AC_SUBST([waimeastylesdir])

fluxboxdir='$(datadir)/fluxbox'
AC_SUBST([fluxboxdir])

fluxboxbgdir='$(fluxboxdir)/backgrounds'
AC_SUBST([fluxboxbgdir])

fluxboxstylesdir='$(fluxboxdir)/styles'
AC_SUBST([fluxboxstylesdir])

blackboxdir='$(datadir)/blackbox'
AC_SUBST([blackboxdir])

blackboxbgdir='$(blackboxdir)/backgrounds'
AC_SUBST([blackboxbgdir])

blackboxstylesdir='$(blackboxdir)/styles'
AC_SUBST([blackboxstylesdir])

icewmdir='$(datadir)/icewm'
AC_SUBST([icewmdir])

icewmthemesdir='$(icewmdir)/themes'
AC_SUBST([icewmthemesdir])

themesdir='$(datadir)/themes'
AC_SUBST([themesdir])

wmakerdir='$(datadir)/WindowMaker'
AC_SUBST([wmakerdir])

wmakerbgdir='$(wmakerdir)/Backgrounds'
AC_SUBST([wmakerbgdir])

wmakerstylesdir='$(wmakerdir)/Styles'
AC_SUBST([wmakerstylesdir])

wmakerthemesdir='$(wmakerdir)/Themes'
AC_SUBST([wmakerthemesdir])

wmakerthemedir='$(wmakerthemesdir)/$(style).themed'
AC_SUBST([wmakerthemedir])

fvwmdir='$(datadir)/fvwm'
AC_SUBST([fvwmdir])
themesdir='$(datadir)/themes'
AC_SUBST([themesdir])

themedir='$(themesdir)/$(style)'
AC_SUBST([themedir])

xdethemedir='$(themesdir)/$(style)/xde'
AC_SUBST([xdethemedir])

imagesdir='$(datadir)/images'
AC_SUBST([imagesdir])

xdeimagedir='$(imagesdir)/$(stylesubdir)'
AC_SUBST([xdeimagedir])

jwmdir='$(datadir)/jwm'
AC_SUBST([jwmdir])
jwmstylesdir='$(jwmdir)/styles'
AC_SUBST([jwmstylesdir])
jwmthemesdir='$(jwmdir)/themes'
AC_SUBST([jwmthemesdir])

pekwmdir='$(datadir)/pekwm'
AC_SUBST([pekwmdir])
pekwmthemesdir='$(pekwmdir)/themes'
AC_SUBST([pekwmthemesdir])

ctwmdir='$(datadir)/ctwm'
AC_SUBST([ctwmdir])
ctwmstylesdir='$(ctwmdir)/styles'
AC_SUBST([ctwmstylesdir])

vtwmdir='$(datadir)/vtwm'
AC_SUBST([vtwmdir])
vtwmstylesdir='$(vtwmdir)/styles'
AC_SUBST([vtwmstylesdir])

twmdir='$(datadir)/twm'
AC_SUBST([twmdir])
twmstylesdir='$(twmdir)/styles'
AC_SUBST([twmstylesdir])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT

# vim: set ft=config:
