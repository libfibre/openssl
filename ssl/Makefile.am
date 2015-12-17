SUBDIRS = record

lib_LIBRARIES = ssl

$(eval ssl_CFLAGS = $(OPENSSL_CFLAGS))
ssl_PREREQS = $(OPENSSL_PREREQS)

ssl_SOURCES = s3_srvr.c s3_clnt.c s3_lib.c s3_enc.c
ssl_SOURCES += s3_both.c s3_cbc.c s3_msg.c t1_meth.c t1_srvr.c t1_clnt.c
ssl_SOURCES += t1_lib.c t1_enc.c t1_ext.c d1_meth.c d1_srvr.c d1_clnt.c d1_lib.c
ssl_SOURCES += d1_msg.c d1_both.c d1_srtp.c ssl_lib.c
ssl_SOURCES += ssl_err2.c ssl_cert.c ssl_sess.c ssl_ciph.c ssl_stat.c ssl_rsa.c
ssl_SOURCES += ssl_asn1.c ssl_txt.c ssl_algs.c ssl_conf.c bio_ssl.c ssl_err.c
ssl_SOURCES += t1_reneg.c tls_srp.c t1_trce.c ssl_utst.c
