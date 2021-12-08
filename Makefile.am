
ACLOCAL_AMFLAGS = -I m4

AUTOMAKE_OPTIONS = nostdinc

EXTRA_DIST = INSTALL COPYING AUTHORS NEWS README README.md README.md.in THANKS TODO ChangeLog RELEASE RELEASE.md

dist_noinst_SCRIPTS = gennews.sh autogen.sh configure.sh rebuild.sh dist.sh

DISTCLEANFILES = ChangeLog AUTHORS NEWS README README.md README.html README.txt RELEASE RELEASE.html RELEASE.txt

dist-hook:
	$(AM_V_GEN)if test -x "`which git 2>/dev/null`" -a -d "$(srcdir)/.git" ; then \
		chmod u+w $(distdir)/{ChangeLog,AUTHORS,NEWS} ; \
		( cd $(srcdir) ; \
		  echo -e "# created with git log --stat=76 -M -C -500|fmt -sct -w80\n" ; \
		  git log --stat=76 -M -C -500|fmt -sct -w80 \
		)|head -10000>$(distdir)/ChangeLog ; \
		( cd $(srcdir) ; \
		  echo "$(PACKAGE) -- authors file.  $(DATE)" ; \
		  echo "" ; \
		  git log|grep '^Author:'|awk '{if(!authors[$$0]){print$$0;authors[$$0]=1;}}' \
		)>$(distdir)/AUTHORS ; \
		( cd $(srcdir) ; \
		  echo "$(PACKAGE) -- history of user-visible changes.  $(DATE)" ; \
		  PACKAGE="$(PACKAGE)" $(srcdir)/gennews.sh \
		)>$(distdir)/NEWS ; \
	fi ; \
	chmod u+w $(distdir)/{README.md,README} ; \
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g;s:\@BRANCH\@:$(BRANCH):g' $(distdir)/README.md.in >$(distdir)/README.md ; \
	cat $(distdir)/README.md | fmt -sct -w80 -g72 >$(distdir)/README

ChangeLog:
	$(AM_V_GEN)if test -x "`which git 2>/dev/null`" -a -d "$(srcdir)/.git" ; then \
		( cd $(srcdir) ; \
		  echo -e "# created with git log --stat=76 -M -C -500|fmt -sct -w80\n" ; \
		  git log --stat=76 -M -C -500|fmt -sct -w80 \
		)|head -10000>$@ ; \
	else touch $@ ; fi

AUTHORS:
	$(AM_V_GEN)if test -x "`which git 2>/dev/null`" -a -d "$(srcdir)/.git" ; then \
		( cd $(srcdir) ; \
		  echo "$(PACKAGE) -- authors file.  $(DATE)" ; \
		  echo "" ; \
		  git log|grep '^Author:'|awk '{if(!authors[$$0]){print$$0;authors[$$0]=1;}}' \
		)>$@ ; \
	else touch $@ ; fi

NEWS:
	$(AM_V_GEN)if test -x "`which git 2>/dev/null`" -a -d "$(srcdir)/.git" ; then \
		( cd $(srcdir) ; \
		  echo "$(PACKAGE) -- history of user-visible changes.  $(DATE)" ; \
		  PACKAGE="$(PACKAGE)" $(srcdir)/gennews.sh \
		)>$@ ; \
	else touch $@ ; fi

index.md: README.md
	$(AM_V_GEN)(echo -e "---\nlayout: default\n---"; cat $<) >$@

README.md: README.md.in
	$(AM_V_GEN)sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g;s:\@BRANCH\@:$(BRANCH):g' $< >$@

README: README.md
	$(AM_V_GEN)cat $< | fmt -sct -w80 -g72 >$@

README.html: README.md
	$(AM_V_GEN)$(MARKDOWN) $< >$@

README.txt: README.html
	$(AM_V_GEN)$(LINKS) -dump -width 80 -nolist $< | sed -r -e 's,^[[:space:]]*,,' >$@

RELEASE: RELEASE.md
	$(AM_V_GEN)cat $< | fmt -sct -w80 -g72 >$@

RELEASE.html: RELEASE.md
	$(AM_V_GEN)$(MARKDOWN) $< >$@

RELEASE.txt: RELEASE.html
	$(AM_V_GEN)$(LINKS) -dump -width 80 -nolist $< | sed -r -e 's,^[[:space:]]*,,' >$@

NOTES.html: NOTES
	$(AM_V_GEN)$(ASCIIDOC) -o - $< >$@

TODO.html: TODO
	$(AM_V_GEN)$(ASCIIDOC) -o - $< >$@

dist_xdetheme_DATA = \
	theme/theme.ini \
	theme/themerc

dist_wmakertheme_DATA = \
	theme/style

dist_xdeimage_DATA = \
	images/blackbird_afterburn.jpg \
	images/blackbird_beale.jpg \
	images/blackbird_climbing.jpg \
	images/blackbird_clouds.jpg \
	images/blackbird_drone.jpg \
	images/blackbird_fields.jpg \
	images/blackbird_highalt.jpg \
	images/blackbird_landing.jpg \
	images/blackbird_liftoff.jpg \
	images/blackbird_mountains.jpg \
	images/blackbird_nose.jpg \
	images/blackbird_oversnow.jpg \
	images/blackbird_peaks.jpg \
	images/blackbird_photos.jpg \
	images/blackbird_piggyback.jpg \
	images/blackbird_pulse.jpg \
	images/blackbird_refuel.jpg \
	images/blackbird_runway.jpg \
	images/blackbirds_flats.jpg \
	images/blackbirds_mist.jpg \
	images/blackbirds_parked.jpg \
	images/blackbirds_suits.jpg \
	images/blackbird_takeoff.jpg \
	images/blackbird_tarmac.jpg \
	images/blackbird_valley.jpg

EXTRA_DIST += \
	images/blackbird_afterburn.jpg \
	images/blackbird_beale.jpg \
	images/blackbird_climbing.jpg \
	images/blackbird_clouds.jpg \
	images/blackbird_drone.jpg \
	images/blackbird_fields.jpg \
	images/blackbird_highalt.jpg \
	images/blackbird_landing.jpg \
	images/blackbird_liftoff.jpg \
	images/blackbird_mountains.jpg \
	images/blackbird_nose.jpg \
	images/blackbird_oversnow.jpg \
	images/blackbird_peaks.jpg \
	images/blackbird_photos.jpg \
	images/blackbird_piggyback.jpg \
	images/blackbird_pulse.jpg \
	images/blackbird_refuel.jpg \
	images/blackbird_runway.jpg \
	images/blackbirds_flats.jpg \
	images/blackbirds_mist.jpg \
	images/blackbirds_parked.jpg \
	images/blackbirds_suits.jpg \
	images/blackbird_takeoff.jpg \
	images/blackbird_tarmac.jpg \
	images/blackbird_valley.jpg

install-data-hook:
	$(MKDIR_P) $(DESTDIR)$(adwmstylesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(adwmstylesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(waimeastylesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(waimeastylesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(fluxboxstylesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(fluxboxstylesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(blackboxstylesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(blackboxstylesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(icewmthemesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(icewmthemesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(jwmthemesdir)
	$(LN_S) ../styles/$(basestyle) $(DESTDIR)$(jwmthemesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(ctwmstylesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(ctwmstylesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(vtwmstylesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(vtwmstylesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(twmstylesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(twmstylesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(pekwmthemesdir)
	$(LN_S) $(basestyle) $(DESTDIR)$(pekwmthemesdir)/$(style)
	$(MKDIR_P) $(DESTDIR)$(themedir)
	$(LN_S) ../$(basestyle)/openbox-3 $(DESTDIR)$(themedir)/openbox-3
	$(MKDIR_P) $(DESTDIR)$(themedir)
	$(LN_S) ../$(basestyle)/gtk-2.0 $(DESTDIR)$(themedir)/gtk-2.0
	$(MKDIR_P) $(DESTDIR)$(wmakerthemedir)
	$(MKDIR_P) $(DESTDIR)$(fluxboxbgdir)
	$(MKDIR_P) $(DESTDIR)$(blackboxbgdir)
	$(MKDIR_P) $(DESTDIR)$(wmakerbgdir)
	$(MKDIR_P) $(DESTDIR)$(xdeimagedir)
	for p in $(dist_xdeimage_DATA) ; do \
		f=$$(basename $$p .jpg) ; \
		install -m644 $(top_srcdir)/images/$$f.jpg $(DESTDIR)$(xdeimagedir)/$$f.jpg ; \
		$(LN_S) ../../../images/$(stylesubdir)/$$f.jpg $(DESTDIR)$(wmakerthemedir)/$$f.jpg ; \
		$(LN_S) ../../images/$(stylesubdir)/$$f.jpg $(DESTDIR)$(fluxboxbgdir)/$$f.jpg ; \
		$(LN_S) ../../images/$(stylesubdir)/$$f.jpg $(DESTDIR)$(blackboxbgdir)/$$f.jpg ; \
		$(LN_S) ../../images/$(stylesubdir)/$$f.jpg $(DESTDIR)$(wmakerbgdir)/$$f.jpg ; \
	done
	for f in $(baseprefix)back $(baseprefix)icon $(baseprefix)tbar $(baseprefix)tile ; do \
		$(LN_S) ../../../WindowMaker/Pixmaps/$$f.xpm $(DESTDIR)$(wmakerthemedir)/$$f.xpm ; \
	done

