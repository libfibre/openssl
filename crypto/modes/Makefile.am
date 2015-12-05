lib_LIBRARIES = crypto

crypto_SOURCES = cbc128.c ctr128.c cts128.c cfb128.c ofb128.c gcm128.c ccm128.c
crypto_SOURCES += xts128.c wrap128.c ocb128.c

$(eval $(call perl_asm,ghash_x86_64,asm/ghash-x86_64.pl,crypto))
$(eval $(call perl_asm,aesni_gcm_x86_64,asm/aesni-gcm-x86_64.pl,crypto))
