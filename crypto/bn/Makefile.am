lib_LIBRARIES = crypto

crypto_SOURCES = bn_add.c bn_div.c bn_exp.c bn_lib.c bn_ctx.c bn_mul.c bn_mod.c
crypto_SOURCES += bn_print.c bn_rand.c bn_shift.c bn_word.c bn_blind.c bn_kron.c
crypto_SOURCES += bn_sqrt.c bn_gcd.c bn_prime.c bn_err.c bn_sqr.c
crypto_SOURCES += rsaz_exp.c bn_recp.c bn_mont.c bn_mpi.c bn_exp2.c bn_gf2m.c
crypto_SOURCES += bn_nist.c bn_depr.c bn_const.c bn_x931p.c bn_intern.c bn_dh.c
crypto_SOURCES += bn_srp.c

$(eval $(call perl_asm,x86_64_mont,asm/x86_64-mont.pl,crypto))
$(eval $(call perl_asm,x86_64_mont5,asm/x86_64-mont5.pl,crypto))
$(eval $(call perl_asm,x86_64_gf2m,asm/x86_64-gf2m.pl,crypto))
$(eval $(call perl_asm,rsaz_x86_64,asm/rsaz-x86_64.pl,crypto))
$(eval $(call perl_asm,rsaz_avx2,asm/rsaz-avx2.pl,crypto))

# Special case. This file is not run through perl-asm but is compiled directly,
# yet it's in the asm sub-directory. Doh. The build will handle this if it's an
# absolute path. NB: we need to use eval.
$(eval crypto_SOURCES += $(THISDIR)/asm/x86_64-gcc.c)
