NU = VIII
MI = Missa$(NU)
KY = Kyrie$(NU)
GL = Gloria$(NU)
SA = Sanctus$(NU)
AD = AgnusDei$(NU)

../$(MI).pdf: $(MI).pdf
	mv $< $@

$(MI).pdf: $(MI).tex $(KY).gtex $(GL).gtex $(SA).gtex $(AD).gtex
	lualatex $<

%.gtex: %.gabc
	gregorio -v $< -o $@

cleanpdf: ../$(MI).pdf
	rm $@

clean:
	rm *.log *.aux *.gaux *.gtex

.PHONY = clean cleanpdf
