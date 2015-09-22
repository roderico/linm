suppbindir = $(bindir)

noinst_DATA = colorset.cfg default.cfg keyset.cfg linm.csh.in linm.sh.in \
	linm_alias.csh.in linm_alias.sh.in qtkeyset.cfg
					
noinst_SCRIPTS = linm_alias.sh linm_alias.csh
suppbin_SCRIPTS = linm.sh linm.csh 

CLEANFILES = linm.sh linm_alias.sh linm.csh linm_alias.csh

EXTRA_DIST = $(noinst_DATA)              

linm.sh: $(srcdir)/linm.sh.in
	sed "s%@""bindir@%$(bindir)%" $(srcdir)/linm.sh.in > linm.sh
	
linm.csh: $(srcdir)/linm.csh.in
	sed "s%@""bindir@%$(bindir)%" $(srcdir)/linm.csh.in > linm.csh
		
linm_alias.sh: $(srcdir)/linm_alias.sh.in
	sed "s%@""bindir@%$(bindir)%" $(srcdir)/linm_alias.sh.in > linm_alias.sh
	
linm_alias.csh: $(srcdir)/linm_alias.csh.in
	sed "s%@""bindir@%$(bindir)%" $(srcdir)/linm_alias.csh.in > linm_alias.csh
