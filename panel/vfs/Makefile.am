METASOURCES = AUTO

SUBDIRS = ftp archive libssh2 samba

noinst_HEADERS = dirreader.h vfsplugin.h
libvfsplugin_a_SOURCES = dirreader.cpp vfsplugin.cpp
noinst_LIBRARIES = libvfsplugin.a

INCLUDES = -I$(top_srcdir)/lib -I$(top_srcdir)/panel/common \
	-I$(top_srcdir)/panel/vfs -I$(top_srcdir)/panel/vfs/archive -I$(top_srcdir)/panel/vfs/ftp \
	-I$(top_srcdir)/panel/vfs/libssh2 -I$(top_srcdir)/panel/vfs/samba


