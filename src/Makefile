SRC = \
	ltxhtml_ltximage.mli \
	ltxhtml_ltximage.ml \
	ltxhtml.ml

.PHONY: all clean install

all:
	ocamlc -I +ocamldoc -o ltxhtml.cma -a $(SRC)
	ocamlopt -I +ocamldoc -o ltxhtml.cmxs -shared $(SRC)

clean:
	rm -rf *.cmi *.cmo *.cma

install: all
	cp ltxhtml.cma ltxhtml.cmxs $$(ocamldoc -customdir)
