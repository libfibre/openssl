lib_LIBRARIES = crypto

crypto_SOURCES = aes_misc.c aes_ecb.c aes_cfb.c aes_ofb.c aes_ige.c aes_wrap.c

$(eval $(call perl_asm,aes_x86_64,asm/aes-x86_64.pl,crypto))
$(eval $(call perl_asm,vpaes_x86_64,asm/vpaes-x86_64.pl,crypto))
$(eval $(call perl_asm,bsaes_x86_64,asm/bsaes-x86_64.pl,crypto))
$(eval $(call perl_asm,aesni_x86_64,asm/aesni-x86_64.pl,crypto))
$(eval $(call perl_asm,aesni_sha1_x86_64,asm/aesni-sha1-x86_64.pl,crypto))
$(eval $(call perl_asm,aesni_sha256_x86_64,asm/aesni-sha256-x86_64.pl,crypto))
$(eval $(call perl_asm,aesni_mb_x86_64,asm/aesni-mb-x86_64.pl,crypto))
