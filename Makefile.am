
AUTOMAKE_OPTIONS = nostdinc

dist_xdetheme_DATA = \
	theme/theme.ini

dist_wmakertheme_DATA = \
	theme/style

dist_xdeimage_DATA = \
	images/blackbird_beale.jpg \
	images/blackbird_clouds.jpg \
	images/blackbird_drone.jpg \
	images/blackbird_fields.jpg \
	images/blackbird_highalt.jpg \
	images/blackbird_mountains.jpg \
	images/blackbird_refuel.jpg \
	images/blackbirds_flats.jpg \
	images/blackbirds_mist.jpg \
	images/blackbirds_parked.jpg \
	images/blackbirds_suits.jpg \
	images/blackbird_takeoff.jpg \
	images/blackbird_tarmac.jpg

EXTRA_DIST = \
	images/blackbird_beale.jpg \
	images/blackbird_clouds.jpg \
	images/blackbird_drone.jpg \
	images/blackbird_fields.jpg \
	images/blackbird_highalt.jpg \
	images/blackbird_mountains.jpg \
	images/blackbird_refuel.jpg \
	images/blackbirds_flats.jpg \
	images/blackbirds_mist.jpg \
	images/blackbirds_parked.jpg \
	images/blackbirds_suits.jpg \
	images/blackbird_takeoff.jpg \
	images/blackbird_tarmac.jpg

install-data-hook:
	mkdir -p $(DESTDIR)$(fluxboxstylesdir)
	ln -s $(basestyle) $(DESTDIR)$(fluxboxstylesdir)/$(style)
	mkdir -p $(DESTDIR)$(blackboxstylesdir)
	ln -s $(basestyle) $(DESTDIR)$(blackboxstylesdir)/$(style)
	mkdir -p $(DESTDIR)$(icewmthemesdir)
	ln -s $(basestyle) $(DESTDIR)$(icewmthemesdir)/$(style)
	mkdir -p $(DESTDIR)$(jwmthemesdir)
	ln -s ../styles/$(basestyle) $(DESTDIR)$(jwmthemesdir)/$(style)
	mkdir -p $(DESTDIR)$(ctwmstylesdir)
	ln -s $(basestyle) $(DESTDIR)$(ctwmstylesdir)/$(style)
	mkdir -p $(DESTDIR)$(vtwmstylesdir)
	ln -s $(basestyle) $(DESTDIR)$(vtwmstylesdir)/$(style)
	mkdir -p $(DESTDIR)$(twmstylesdir)
	ln -s $(basestyle) $(DESTDIR)$(twmstylesdir)/$(style)
	mkdir -p $(DESTDIR)$(pekwmthemesdir)
	ln -s $(basestyle) $(DESTDIR)$(pekwmthemesdir)/$(style)
	mkdir -p $(DESTDIR)$(themedir)
	ln -s ../$(basestyle)/openbox-3 $(DESTDIR)$(themedir)/openbox-3
	mkdir -p $(DESTDIR)$(themedir)
	ln -s ../$(basestyle)/gtk-2.0 $(DESTDIR)$(themedir)/gtk-2.0
	mkdir -p $(DESTDIR)$(wmakerthemedir)
	mkdir -p $(DESTDIR)$(fluxboxbgdir)
	mkdir -p $(DESTDIR)$(blackboxbgdir)
	mkdir -p $(DESTDIR)$(wmakerbgdir)
	mkdir -p $(DESTDIR)$(xdeimagedir)
	for p in $(dist_xdeimage_DATA) ; do \
		f=$$(basename $$p .jpg) ; \
		install -m644 $(top_srcdir)/images/$$f.jpg $(DESTDIR)$(xdeimagedir)/$$f.jpg ; \
		ln -s ../../../images/$(stylesubdir)/$$f.jpg $(DESTDIR)$(wmakerthemedir)/$$f.jpg ; \
		ln -s ../../images/$(stylesubdir)/$$f.jpg $(DESTDIR)$(fluxboxbgdir)/$$f.jpg ; \
		ln -s ../../images/$(stylesubdir)/$$f.jpg $(DESTDIR)$(blackboxbgdir)/$$f.jpg ; \
		ln -s ../../images/$(stylesubdir)/$$f.jpg $(DESTDIR)$(wmakerbgdir)/$$f.jpg ; \
	done
	for f in $(baseprefix)back $(baseprefix)icon $(baseprefix)tbar $(baseprefix)tile ; do \
		ln -s ../../../WindowMaker/Pixmaps/$$f.xpm $(DESTDIR)$(wmakerthemedir)/$$f.xpm ; \
	done

