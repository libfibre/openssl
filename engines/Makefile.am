SUBDIRS = ccgost

lib_LIBRARIES = crypto

crypto_SOURCES = e_4758cca.c e_gmp.c e_padlock.c e_capi.c e_ossltest.c

$(eval $(call perl_asm,e_padlock_x86_64,asm/e_padlock-x86_64.pl,crypto))
