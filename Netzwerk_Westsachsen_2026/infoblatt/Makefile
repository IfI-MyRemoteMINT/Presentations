# A4-Infoblatt MyRemoteMINT (TUBAF-Stil)
# Voraussetzungen: pandoc, xelatex, qrencode, Schrift Lato (sonst TeX Gyre Heros)
#
#   make        -> baut infoblatt.pdf
#   make qr     -> erzeugt die QR-Codes neu
#   make clean  -> entfernt das PDF

QRENCODE := qrencode --type=PNG32 -s 12 -m 2 --foreground=004F9Fff --background=ffffffff

all: infoblatt.pdf

infoblatt.pdf: infoblatt.md tubaf-template.tex qr/calliope.png qr/ledring.png qr/vortrag.png
	pandoc --from=markdown+raw_tex --template=tubaf-template.tex --pdf-engine=xelatex --resource-path=.:qr -o $@ $<

qr:
	@mkdir -p qr
	$(QRENCODE) -o qr/calliope.png "https://edrys-labs.github.io/?/classroom/j83SVIVcOd5ARUtd"
	$(QRENCODE) -o qr/ledring.png "https://edrys-labs.github.io/?/classroom/sEHRNUR9TnhA8wYs"
	$(QRENCODE) -o qr/vortrag.png "https://liascript.github.io/course/?https://raw.githubusercontent.com/IfI-MyRemoteMINT/Presentations/main/Netzwerk_Westsachsen_2026/presentation.md"

clean:
	rm -f infoblatt.pdf

.PHONY: all qr clean
