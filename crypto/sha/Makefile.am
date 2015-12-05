lib_LIBRARIES = crypto

crypto_SOURCES = sha1dgst.c sha1_one.c sha256.c sha512.c

$(eval $(call perl_asm,sha1_x86_64,asm/sha1-x86_64.pl,crypto))
$(eval $(call perl_asm,sha1-mb_x86_64,asm/sha1-mb-x86_64.pl,crypto))
$(eval $(call perl_asm,sha256-mb_x86_64,asm/sha256-mb-x86_64.pl,crypto))

# Crap. asm/sha512-x86_64.pl bucks the trend. Rather than taking the form;
#
#     perl whatever.pl elf > whatever.s
#
# It uses;
#
#     perl whatever.pl elf whatever.s
#
# It looks like this is because there's a single sha512-x86_64.pl that
# generates assembly for 256-bit and 512-bit variants depending on the name of
# the output file. I'm not tweaking input files, just build files, so I'll add
# complexity here to work around this. But clearly it's something that could be
# simplified if the perl-asm file-level interface was consolidated.
# (NOTE: the only difference between this routine and the regular 'perl_asm' is
# the lack of a ">" redirect in the command-line to invoke perl.)
define perl_asm_sha512
  $(eval $(3)_$(1)_input = $(THISDIR)/$(2))
  $(eval $(3)_$(1)_output = $(OPENSSL_OUTDIR1)/$(1).s)
  $(eval OUTS += $($(3)_$(1)_output))
  $(eval $(3)_SOURCES += $($(3)_$(1)_output))
$($(3)_$(1)_output): $($(3)_$(1)_input) | $(OPENSSL_DIR1)
	perl $($(3)_$(1)_input) elf $($(3)_$(1)_output)
endef

$(eval $(call perl_asm,sha256_x86_64,asm/sha512-x86_64.pl,crypto))
$(eval $(call perl_asm,sha512_x86_64,asm/sha512-x86_64.pl,crypto))
