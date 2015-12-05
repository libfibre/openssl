bin_BINARIES = openssl

$(eval openssl_CFLAGS = $(OPENSSL_CFLAGS))
$(eval openssl_CFLAGS += -I$(OPENSSL_TOP)/include -I$(OPENSSL_TOP))

openssl_SOURCES = openssl.c asn1pars.c ca.c ciphers.c cms.c crl.c crl2p7.c
openssl_SOURCES += dgst.c dhparam.c dsa.c dsaparam.c ec.c ecparam.c enc.c
openssl_SOURCES += engine.c errstr.c gendsa.c genpkey.c genrsa.c nseq.c ocsp.c
openssl_SOURCES += passwd.c pkcs12.c pkcs7.c pkcs8.c pkey.c pkeyparam.c
openssl_SOURCES += pkeyutl.c prime.c rand.c req.c rsa.c rsautl.c s_client.c
openssl_SOURCES += s_server.c s_time.c sess_id.c smime.c speed.c spkac.c srp.c
openssl_SOURCES += ts.c verify.c version.c x509.c apps.c opt.c s_cb.c s_socket.c
openssl_SOURCES += app_rand.c
openssl_LDADD = ssl crypto
openssl_LINKFLAGS = -ldl
