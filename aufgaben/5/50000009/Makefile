#
# build domain image for problem 90000009
#
domain = domain-1.pdf
	
$(domain): domain.mp
	TEX=latex mpost domain.mp
	for f in domain.?; \
	do \
		mptopdf $${f}; \
	done

loes.png:	loes.pov
	povray -A0.1 -R20 -W3840 -H2160 loes.pov

loes.jpg:	loes.png
	convert -extract 1927x1740+828+300 loes.png -resize 50% \
		-density 300 -units PixelsPerInch loes.jpg

