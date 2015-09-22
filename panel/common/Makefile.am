INCLUDES = -I$(top_srcdir)/lib -I$(top_srcdir)/panel \
	-I$(top_srcdir)/panel/common -I$(top_srcdir)/panel/vfs -I$(top_srcdir)/panel/vfs/ftp \
	-I$(top_srcdir)/panel/vfs/archive
METASOURCES = AUTO
noinst_LIBRARIES = libpanelcommon.a
libpanelcommon_a_SOURCES = colorcfgload.cpp keycfgload.cpp mlscfgload.cpp \
						panel.cpp mcd.cpp selection.cpp history.cpp remotecfgload.cpp passencrypt.cpp
noinst_HEADERS = colorcfgload.h colorentry.h keycfgload.h mlscfgload.h file.h \
			sortfile.h reader.h readerctl.h panel.h mcd.h mpool.h selection.h history.h \
	remotecfgload.h passencrypt.h

