MI = MissaVIII
KY = KyrieVIII
GL = GloriaVIII
SA = SanctusVIII
AD = AgnusDeiVIII

$(MI).pdf: $(MI).tex $(KY).gtex 
	lualatex $<

%.gtex: %.gabc
	gregorio -v $< -o $@

cleanpdf:
	rm $(MI).pdf

clean:
	rm *.log *.aux *.gaux *.gtex

.PHONY = clean cleanpdf
