# hilbertmodularsurfacesdata


Repository for the data associated to

- [A database of basic numerical invariants of Hilbert modular surfaces](https://arxiv.org/abs/2301.10302) by
[Eran Assaf](https://math.dartmouth.edu/~eassaf/),
[Angelica Babei](https://angelicababei.com/),
[Ben Breen](http://www.benbreenmath.com/),
[Edgar Costa](https://edgarcosta.org),
[Juanita Duque-Rosero](https://math.dartmouth.edu/~jduque/),
[Aleksander Horawa](https://people.maths.ox.ac.uk/horawa/),
[Jean Kieffer](https://scholar.harvard.edu/kieffer),
[Avinash Kulkarni](https://math.dartmouth.edu/~akulkarn/),
[Grant Molnar](https://www.grantmolnar.com/),
[Sam Schiavone](https://math.mit.edu/~sschiavo/), and
[John Voight](http://www.math.dartmouth.edu/~jvoight/)

The data was computed with the Magma package [hilbertmodularforms](https://github.com/edgarcosta/hilbertmodularforms/)

## Labels

In a given file, each row contains data pertaining to a particular Hilbert modular surface. The first entry in each such row is a label identifying the surface. The label is of the form `field_label-level_label-component_label-ambient_type-gamma_type`where
* `field_label` is the [LMFDB label](https://www.lmfdb.org/knowledge/show/nf.label) of the real quadratic field $F$ associated to the surface;
* `level_label` is the [LMFDB label](https://www.lmfdb.org/knowledge/show/nf.ideal_labels) of the level $\mathfrak{N}$;
*  `component_label` is the [LMFDB label](https://www.lmfdb.org/knowledge/show/nf.ideal_labels) of the ideal $\mathfrak{b}$ specifying a component of the surface;
* `ambient_type` is either `gl` or `sl` depending on whether the associated Hilbert modular group is defined as a subset of $\operatorname{GL}_2^+(F)$ or $\operatorname{SL}_2(F)$
* `gamma_type` is either `0`, `1`, or `f` according as the Hilbert modular group is $\Gamma_0(\mathfrak{N})$, $\Gamma_1(\mathfrak{N})$, or $\Gamma(\mathfrak{N})$ (or the $\operatorname{SL}$ variants of these).

## File formats

* Files with names ending in `inv.txt` contain data of geometric invariants of the surfaces. Each row is of the form `label:[h[0,2],h[1,1]]:K^2:chi`, where
  * `label` is the label of the surface;
  * `h[0,2]` and `h[1,1]` are the Hodge numbers $h^{0,2}$ and $h^{1,1}$;
  * `K^2` is the self-intersection number of the canonical divisor; and
  * `chi`is the holomorphic Euler characteristic (what van der Geer calls the arithmetic genus)

* Files with names ending in `kposs.txt` contain data of the possible Kodaira dimensions of each surface. Each row is of the form `label:ks`, where
  * `label` is the label of the surface; and
  * `ks` are the possible values of the Kodaira dimension $\kappa$ of the surface.

* Files with names ending in `cusps.txt` contain data about the cusps on the surfaces. Each row contains data on one cusp and is of the form `label:component-label:M-label:[[a1,a2],[b1,b2]]:bs:v`, where
  * `label` is the label of the surface;
  * `component-label` is the [LMFDB label](https://www.lmfdb.org/knowledge/show/nf.ideal_labels) of the ideal $\mathfrak{b}$ specifying a component of the surface;
  * `M-label` is the [LMFDB label](https://www.lmfdb.org/knowledge/show/nf.ideal_labels) of the ideal $\mathfrak{M}$ associated to the cusp; see equation 3.1.2 in the section Cusps;
  * `[[a1,a2],[b1,b2]]` indicate the coordinates of the cusp $(a_1 + a_2 w : b_1 + b_2 w)$ as points in $\mathbb{P}^1(F)$, where $F = \mathbb{Q}(w)$;
  * `bs` gives the periodic part of the associated Hirzebruch-Jung continued fraction; equivalently, the self-intersection numbers of the curves in the resolution of the cusp; and
  * `v` is the number of times `bs` must be repeated to cover every curve in the resolution.

* Files with names ending in `hs.txt` contain data about the Hilbert series of each surface. Here Hilbert series are represented as rational functions in `x`. Each row is of the form `label:num:den`, where
  * `label` is the label of the surface;
  * `num` is the numerator of the Hilbert series; and
  * `den` is the denominator of the Hilbert series.
