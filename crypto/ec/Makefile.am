lib_LIBRARIES = crypto

crypto_SOURCES = ec_lib.c ecp_smpl.c ecp_mont.c ecp_nist.c ec_cvt.c ec_mult.c
crypto_SOURCES += ec_err.c ec_curve.c ec_check.c ec_print.c ec_asn1.c ec_key.c
crypto_SOURCES += ec2_smpl.c ec2_mult.c ec_ameth.c ec_pmeth.c eck_prn.c
crypto_SOURCES += ecp_nistp224.c ecp_nistp256.c ecp_nistp521.c ecp_nistputil.c
crypto_SOURCES += ecp_oct.c ec2_oct.c ec_oct.c ecp_nistz256.c

$(eval $(call perl_asm,ecp_nistz256_x86_64,asm/ecp_nistz256-x86_64.pl,crypto))
