PROG := krfctl

all: gentable $(PROG)

.PHONY: gentable
gentable:
	ruby gentable

.PHONY: genprofiles
genprofiles:
	ruby genprofiles

table.gen.c: gentable
profiles.gen.c: genprofiles

$(PROG): $(PROG).o table.gen.o profiles.gen.o

.PHONY: clean
clean:
	rm -f $(PROG) *.o
	rm -f *.gen.c # gentable/genprofiles files
