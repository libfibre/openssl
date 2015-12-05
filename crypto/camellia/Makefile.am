lib_LIBRARIES = crypto

crypto_SOURCES = cmll_ecb.c cmll_ofb.c cmll_cfb.c cmll_ctr.c cmll_misc.c

$(eval $(call perl_asm,cmll_x86_64,asm/cmll-x86_64.pl,crypto))
