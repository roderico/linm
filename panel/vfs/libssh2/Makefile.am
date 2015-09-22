INCLUDES = -I$(top_srcdir)/lib -I$(top_srcdir)/panel/common \
	-I$(top_srcdir)/panel/vfs -I$(top_srcdir)/panel/vfs/archive -I$(top_srcdir)/panel/vfs/ftp \
	-I$(top_srcdir)/panel/vfs/libssh2
	
noinst_HEADERS = libssh2.h libssh2_priv.h libssh2_sftp.h libssh2_publickey.h openssl.h SFtpReader.h

METASOURCES = AUTO	
AM_CFLAGS = -fPIC

if !LINM_UNUSE_SFTP
		
lib_LTLIBRARIES = liblinmpluginsftp.la
liblinmpluginsftp_la_SOURCES = SFtpReader.cpp channel.c comp.c crypt.c hostkey.c kex.c mac.c misc.c \
	packet.c scp.c session.c sftp.c userauth.c openssl.c pem.c publickey.c transport.c
	
endif

EXTRA_DIST = README LICENSE

clean:
	-rm -rf *.o *.a *.la .libs _libs *.lo
 
