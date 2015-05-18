
AUTOMAKE_OPTIONS = nostdinc

dist_xdetheme_DATA = \
	theme/theme.ini \
	theme/themerc

dist_wmakertheme_DATA = \
	theme/style

dist_xdeimage_DATA = \
	images/blackbird_afterburn.jpg \
	images/blackbird_beale.jpg \
	images/blackbird_clouds.jpg \
	images/blackbird_drone.jpg \
	images/blackbird_fields.jpg \
	images/blackbird_highalt.jpg \
	images/blackbird_mountains.jpg \
	images/blackbird_peaks.jpg \
	images/blackbird_pulse.jpg \
	images/blackbird_refuel.jpg \
	images/blackbird_runway.jpg \
	images/blackbirds_flats.jpg \
	images/blackbirds_mist.jpg \
	images/blackbirds_parked.jpg \
	images/blackbirds_suits.jpg \
	images/blackbird_takeoff.jpg \
	images/blackbird_tarmac.jpg

EXTRA_DIST = \
	images/blackbird_afterburn.jpg \
	images/blackbird_beale.jpg \
	images/blackbird_clouds.jpg \
	images/blackbird_drone.jpg \
	images/blackbird_fields.jpg \
	images/blackbird_highalt.jpg \
	images/blackbird_mountains.jpg \
	images/blackbird_peaks.jpg \
	images/blackbird_pulse.jpg \
	images/blackbird_refuel.jpg \
	images/blackbird_runway.jpg \
	images/blackbirds_flats.jpg \
	images/blackbirds_mist.jpg \
	images/blackbirds_parked.jpg \
	images/blackbirds_suits.jpg \
	images/blackbird_takeoff.jpg \
	images/blackbird_tarmac.jpg


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

