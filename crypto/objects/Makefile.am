lib_LIBRARIES = crypto

crypto_SOURCES = o_names.c obj_dat.c obj_lib.c obj_err.c obj_xref.c

$(eval OBJ_DAT_DIR = $(THISDIR))
$(OBJ_DAT_DIR)/obj_dat.h: $(OPENSSL_TOP)/include/openssl/obj_mac.h
	perl $(OBJ_DAT_DIR)/obj_dat.pl $(OPENSSL_TOP)/include/openssl/obj_mac.h $(OBJ_DAT_DIR)/obj_dat.h
