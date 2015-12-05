SUBDIRS = objects md4 md5 sha mdc2 hmac ripemd whrlpool des aes rc2 rc4 idea
SUBDIRS += bf cast camellia seed modes bn ec rsa dsa ecdsa dh ecdh dso engine
SUBDIRS += buffer bio stack lhash rand err evp asn1 pem x509 x509v3 conf txt_db
SUBDIRS += pkcs7 pkcs12 comp ocsp ui cms pqueue ts srp cmac

lib_LIBRARIES = crypto

# We define dependencies that depend on a volatile variable (THISDIR is
# modified inbetween the inclusion of each Makefile.am input.) If we don't use
# eval here, the declarations that depend on THISDIR will all inherit the last
# value of THISDIR (once all the recursive scripted logic has run). Using eval
# forces crypto_CFLAGS to use the value of THISDIR at the time this Makefile.am
# is being included and parsed.
$(eval crypto_CFLAGS = $(OPENSSL_CFLAGS) -I$(OPENSSL_TOP)/include)
$(eval crypto_CFLAGS += -I$(THISDIR)/include -I$(THISDIR)/modes)
$(eval crypto_CFLAGS += -I$(OPENSSL_OUTDIR1) -I$(OPENSSL_TOP))
crypto_PREREQS = $(OPENSSL_TOP)/include/openssl/opensslconf.h

crypto_SOURCES = cryptlib.c mem.c mem_dbg.c cversion.c ex_data.c cpt_err.c
crypto_SOURCES += ebcdic.c uid.c o_time.c o_str.c o_dir.c thr_id.c lock.c fips_ers.c
crypto_SOURCES += o_init.c o_fips.c sec_mem.c

$(eval $(call perl_asm,cpuid_x86_64,x86_64cpuid.pl,crypto))
