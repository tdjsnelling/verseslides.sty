# verseslides.sty

A LaTeX helper to output verse as images, suitable for posting to social media platforms like Instagram.

Requires ImageMagick to be installed and the `magick` executable to be available.

The `verseslide` command creates a [verse](https://texdoc.org/serve/verse.pdf/0) environment, so that's the syntax you should use.

## Usage

Add `verseslides.sty` and `texture.jpg` to your LaTeX project directory or into your system texmf directory.

The following basic example shows the helper in use:

```tex
\documentclass[
	convert={
		density=1500,
		size=1080x1080,
		outext=.png,
		convertexe={magick}
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

Simply add a new `\verseslide{ ... }` for each image you want to produce.

The resulting image will look something like this:

<img src="https://github.com/tdjsnelling/verseslides.sty/assets/6264509/ac6ab828-0d9d-4fa0-8855-ea70390a46af" width="600px" />
