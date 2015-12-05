lib_LIBRARIES = crypto

crypto_SOURCES = o_names.c obj_dat.c obj_lib.c obj_err.c obj_xref.c

$(THISDIR)/obj_dat.h: $(OPENSSL_TOP)/include/openssl/obj_mac.h
	perl $(THISDIR)/obj_dat.pl $(OPENSSL_TOP)/include/openssl/obj_mac.h $(THISDIR)/obj_dat.h
