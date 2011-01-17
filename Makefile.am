VERSION=0.1.0
LANG1=is
LANG2=sv
PREFIX1=$(LANG1)-$(LANG2)
PREFIX2=$(LANG2)-$(LANG1)
BASENAME=apertium-$(PREFIX1)


$(PREFIX1).autobil.bin: $(BASENAME).$(PREFIX1).dix
	apertium-validate-dictionary $(BASENAME).$(PREFIX1).dix
	lt-comp lr $(BASENAME).$(PREFIX1).dix $@

$(PREFIX2).autobil.bin: $(BASENAME).$(PREFIX1).dix
	apertium-validate-dictionary $(BASENAME).$(PREFIX1).dix
	lt-comp rl $(BASENAME).$(PREFIX1).dix $@

apertium_is_svdir=$(prefix)/share/apertium/apertium-$(PREFIX1)/
apertium_is_modesdir=$(prefix)/share/apertium/modes/

apertium_is_sv_DATA=$(PREFIX1).autobil.bin \
                    $(PREFIX2).autobil.bin

