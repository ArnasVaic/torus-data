# Conway's game 'Life' perturbed

This Github folder supplements the article "Conway's game 'Life' perturbed" of Raimundas Vidunas and Arnas Vaicekauskas (Vilnius University).

The main files are `Torus5x5.txt`, `Torus6x6.txt`, `Torus7x7.txt` and `8x8/Torus8x8.txt`, `9x9/Torus9x9.txt`, `10x10/Torus10x10.txt` which list all ground patterns on the considered torus, together with the additional information.

For the toruses of size up to 8x8, the format for presenting each ground pattern X in these main files is the following:

* The 1st row gives the #-rank of the ground pattern, and the island composition of the pattern, following the abbreviations described in the file `Naming_Islands.txt`

* The 2nd row gives this information about the ground pattern:
- `p=..`, the oscillation period (`p=1` for still-lives)
- `c=..`, the number of live cells in the pattern (averaged over the oscillation phases)
- `h=..`, the number of live cell pairs that neighbour along an edge (vertically or horizontally)
- `d=..`, the number of live cell pairs that neighbour along an edge (diagonally)
- `hh=..`, the number of live cell pairs that differ by the vectors $(2,0), (0,2), (-2,0), (0,-2)$
- `dd=..`, the number of live cell pairs that differ by the diagonal vectors $(2,2), (2,-2)$, etc
- `hd=..`, the number of live cell pairs that differ by a move of chess knight

The counting numbers `c`, `h`, `d`, `hh`, `dd`, `hd` are invariants of the pattern under the symmetries of the torus. Along with the island naming (in the 1st row), these numbers could be used for searching and recognising the ground patterns.

* The 3rd row `ev:` gives the numerical component for the pattern X in the leading eigenvector.

* The 4rd row `decays:` enumerates the ground patterns to which the pattern X decays, by their the #-ranks. The pattern X is included in this list.

* The 5rd row `rates:` gives the corresponding rates of X decays to the ground patterns listed in the 4rd row. The corresponding decay rate of X to "itself" is negative.

* The subsequent rows depict the pattern X in a 2-dimensional graphical form. 

For the torus of size 9x9, the data is the same, except that the 3rd row is `ev.r.d.:` instead of `ev:`, meaning the relative difference $(v_{k}-v_{k+1})/v_{k+1}$ to the next ground pattern. In particular, for bunch patterns (and for the last pattern) this difference is $0$. The eigenvector for the 9x9 torus is given numerically (with high precision) in the separate file `9x9/Eigenvector9.txt`

For the torus of size 10x10, these attempts are made to reduce the file size:

- The 4th and 5th rows (for each pattern X) are skipped. The transition matrix 
is given in the separate file `10x10/Matrix10x10.txt`

- The 3rd row is `evrd`, with the same meaning as `ev.r.d.` for the 9x9 torus.
The eigenvector for the 10x10 torus is given numerically (with high precision) 
in the separate file `10x10/Eigenvector10.txt`

- More compact format (with fewer spaces) is applied to the second row and 
the graphical representation of the pattern X.

Besides these files describing the patterns and the transition matrix, the following files are included:

* `8x8/Island_Views_8.txt`, `9x9/Island_Views_9.txt` and `10x10/Island_Views_10.txt`.
These files exemplify all islands occurring in ground patterns on the considered toruses.
The abbreviated code for describing the islands is given in the mentioned file 
`Naming_Islands.txt`

This file displays all oscillating patterns that do not combine with stationary patterns. The phases of oscillators displayed in this file seek to illustrate a minimal set of generating islands for all patterns (as described in Appendix Section A.2), but the island compositions (announced on the first rows of pattern descriptions in the files `Torus8x8.txt`, etc) do not aim at recognising simplest islands in oscillator phases.

* `9x9/Bunches9.txt` and `10x10/Bunches10.txt`. These files describe the bunches (pairs, triples, quartets) of ground patterns with equal eigenvalue components.

* `10x10/Table_A20.txt` and `10x10/Table_A21.txt`. These files provide more complete information 
supplementing the Appendix Tables A.20 and A.21.

Several pictures (in the .jpg format) from the article are added. Additionally, here are high precision numerical expressions for the leading eigenvalues on the considered toruses:

For the 5x5 torus:
$-14.131565573559312929238438976311552701127098597507$

For the 6x6 torus:
$-15.422752476115013329849283806912980751261745334434$

For the 7x7 torus:
$-22.611108307679762666518387412235462697572209824164$

For the 8x8 torus: 
$-9.7898961730637551211082729491351278100190786170030$

For the 9x9 torus:
$-7.02183865966577916060887945844675783955927739664672753406087908700610314778170267$

For the 10x10 torus:
$-8.72146978142499448863808944207377845445981105479799914131756252506049419817991049320059599257611145375470946599907872104239043967130831076475862072135602746988127275735499292600015339$
