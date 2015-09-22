# not a GNU package. You can remove this line, if
# have all needed files, that a GNU package needs
AUTOMAKE_OPTIONS = foreign 1.4

ACLOCAL_AMFLAGS = -I m4

SUBDIRS = intl po lib panel editor src sh

noinst_DATA = README.ko_euckr README.ko_utf8 linm.spec debian/*
EXTRA_DIST = config.rpath m4/ChangeLog  $(noinst_DATA)

install-exec-hook :
	if test -d $(DESTDIR)$(sysconfdir)/profile.d ; then \
		if test -w $(DESTDIR)$(sysconfdir)/profile.d ; then \
			install -c -m 755 $(top_srcdir)/sh/linm_alias.sh $(DESTDIR)$(sysconfdir)/profile.d \
		; fi \
	; fi

	if ! test -d $(DESTDIR)$(LINM_CFGPATH) ; then \
		install -d -m 755 $(DESTDIR)$(LINM_CFGPATH) \
	; fi 

	if test -w $(DESTDIR)$(LINM_CFGPATH) ; then \
		install -c -m 644 $(top_srcdir)/sh/default.cfg \
					$(top_srcdir)/sh/colorset.cfg \
					$(top_srcdir)/sh/keyset.cfg \
					$(DESTDIR)$(LINM_CFGPATH) \
	; else \
		if ! test -d ~/.linm ; then \
			install -d -m 755 ~/.linm \
		; fi && \
		install -c -m 644 $(top_srcdir)/sh/default.cfg \
					$(top_srcdir)/sh/colorset.cfg \
					$(top_srcdir)/sh/keyset.cfg \
					~/.linm \
	; fi

	if ! test -d $(DESTDIR)$(datadir)/pixmaps ; then \
		install -d -m 755 $(DESTDIR)$(datadir)/pixmaps \
	; fi

	if test -w $(DESTDIR)$(datadir)/pixmaps ; then \
		install -c -m 644 $(top_srcdir)/debian/linm.xpm $(DESTDIR)$(datadir)/pixmaps \
	; fi
	
	if ! test -d $(DESTDIR)$(datadir)/applications ; then \
		install -d -m 755 $(DESTDIR)$(datadir)/applications \
	; fi

	if test -w $(DESTDIR)$(datadir)/applications ; then \
		install -c -m 644 $(top_srcdir)/debian/LinM.desktop $(DESTDIR)$(datadir)/applications \
	; fi

uninstall-hook :
	-rm -f $(DESTDIR)$(LINM_CFGPATH)/default.cfg $(DESTDIR)$(LINM_CFGPATH)/keyset.cfg $(DESTDIR)$(LINM_CFGPATH)/colorset.cfg
	-rm -f $(DESTDIR)$(sysconfdir)/profile.d/linm_alias.sh
	-rm -rf ~/.linm
