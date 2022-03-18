From presentation by Gerd Blanke at the Stammtisch...https://www.nfdi4chem.de/index.php/event/stammtisch-chemotion/

# InChI

Single-double bonds not specified... but the number of H is specified.

V2 mol files fully implemented (v3 on the work)
Gerd Blanke https://www.inchi-trust.org/individual/gerd-blanke/
https://www.youtube.com/watch?v=Ke44aIP2bno

InChI Trust financed by editors - very little money.

Used, by EBI, NIH (PubChem), RSC (ChemSpider) Elsevier (Reaxys)

## AuxInfo

Inchi can have atom coordinates and chages... can reconstruct mol from the inchi.


# RInChI
Gerd Blanke https://www.inchi-trust.org/individual/gerd-blanke/
https://www.youtube.com/watch?v=ONHw7uy03tc

Example
```
RInChI=1.00.1S/C2H60/c1-2-3/h3H,2H2,1H3!C4H802/c1-2-3-
4(5)6/h2-3H2,1H3,(H,5,6)<>C6H1202/c1-3-5-6(7)8-4-2/h3-5H2,1-
2H3!H20/hIH2<>H204S/cl-5(2,3)4/h(H2,1,2,3,4)/d=
```

Exclamation : separate compounds, alphabetical
d: info about reaction
"<>" separate groups; alphabetical order
"=" equlibrium "+" left to right, "-" the reverse direction.
## RInChIKey
Different flavors ...
Long-RInChIKey
Short-RInChIKey somewhat shortest
Web-RInChIKey only take mentioned components (h2o may not be in the dispalyed reaction.) Not clear

Each reactant has an InChI
also

## Atom mapping
MapAuxInfo for mapping!


## Stereochemistry
Stereochemistry can described
pu: pure
mix: mixture
rac: racemate
## auxilary information

... JSON reaction data. yield, ph stirring time
... JSON components data. (concentrations, color, density, purity)

Quantities...
