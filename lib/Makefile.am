INCLUDES = -I. -I.. -I../intl -I$(top_srcdir)/intl
METASOURCES = AUTO
noinst_HEADERS = define.h exception.h mlslocale.h strutil.h configure.h \
	mlslog.h mlsmutex.h cmdshell.h mlsthread.h strlinetoken.h mlsdialog.h
noinst_LIBRARIES = libmlscommon.a
libmlscommon_a_SOURCES = exception.cpp mlslocale.cpp configure.cpp strutil.cpp \
		mlslog.cpp mlsmutex.cpp mlsthread.cpp mlsdialog.cpp

localedir = $(datadir)/locale
DEFS = -DLOCALEDIR=\"$(localedir)\" @DEFS@
