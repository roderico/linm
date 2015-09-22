INCLUDES = -I$(top_srcdir)/lib -I$(top_srcdir)/panel/common 	-I$(top_srcdir)/panel/vfs -I$(top_srcdir)/panel/vfs/archive -I$(top_srcdir)/panel/vfs/ftp 	-I$(top_srcdir)/panel/vfs/libssh2
METASOURCES = AUTO

if !LINM_UNUSE_SAMBA

lib_LTLIBRARIES = liblinmpluginsmb.la
liblinmpluginsmb_la_SOURCES = SMBReader.cpp

endif

noinst_HEADERS = SMBReader.h

