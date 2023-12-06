# verseslides.sty

A LaTeX helper to output verse as images, suitable for posting to social media platforms like Instagram.

## Usage

Add `verseslides.sty` and `texture.jpg` to your LaTeX project directory.

The following basic example shows the helper in use:

```tex
\documentclass[
	convert={
		density=1500,
		size=1080x1080,
		outext=.png,
		convertexe={convert}
		%convertexe={magick.exe} % windows
	},
	multi=slide,
	margin=1.5cm,
	tikz,
	12pt
]{standalone}

\usepackage{verseslides}

\begin{document}
	\sbox0{multa quoque et bello passus, dum conderet urbem,} % measure width
	\verseslide{
		Arma virumque cano, Troiae qui primus ab oris\\
		Italiam, fato profugus, Laviniaque venit\\
		litora, multum ille et terris iactatus et alto\\
		vi superum saevae memorem Iunonis ob iram;\\
		multa quoque et bello passus, dum conderet urbem,\\
		inferretque deos Latio, genus unde Latinum,\\
		Albanique patres, atque altae moenia Romae.\\!
	}
\end{document}
```
