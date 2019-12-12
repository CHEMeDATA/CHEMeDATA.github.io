# Chemistry object detector 

We describe here a method aiming at listing the [chemistry objects](chemistry_object.md) found in an archive file (.zip, BagIt, etc.).

These lists are quite preliminary and (purposively) uneven and (in some cases incomplete). The aim is mostly to show the underlying ontology which whould need to be defined (possibly using [OWL](https://www.w3.org/TR/owl2-primer/)?).

The method consists in searching in all folder of the archive for a specific file name (eg. file_name:"`1r`") or filename extention (file_name:"`*.sp`")

## Short list
#|Chemistry object | Criteria | Type of visualization
-|------|---|---
2|Bruker 1D NMR spectrum (generic)|C1=[file_name:"`1r`" & exist_file:"`../../fid`" & exist_file:"`../../acqus`"]|x/y plot (ppm/intensity)
7|IR spectrum|file_name:"`*.sp`"|x/y plot (energy in nm non-homogeneous scale/intensity)
8|X-ray cristallographic structure|file_name:"`*.cif`"|3D chemistry structure visualisation)

## Long list

#|Chemistry object | Criteria | Type of visualization
-|------|---|---
1|Bruker 1D NMR FID|file_name:"fid" & exist_file:"`./acqus`"|x/y plot (time/intensity)
2|Bruker 1D NMR spectrum (generic)|C1=[file_name:"1r" & exist_file:"../../fid" & exist_file:"../../acqus"]|x/y plot (ppm/intensity)
3|Bruker 1D <sup>1</sup>H NMR spectrum|C1 & find_line="##$NUC1= <1H>" in "../../acqus"|x/y plot (1H ppm/intensity/integrals)
4|Bruker 1D <sup>13</sup>C NMR spectrum|C1 & find_line="##$NUC1= <13C>" in "../../acqus"|x/y plot (1H ppm/intensity/peak picking)
5|Bruker 2D NMR spectrum(generic)|C2=[file_name:"2rr" & exist_file:"../../ser" & exist_file:"../../acqus" & & exist_file:"../../acqu2s"]|mesh plot (ppm/ppm/intensity)
6|Bruker 2D NMR HSQC spectrum|C2 & find_line="##$NUC1= <13C>" in "../../acqus" & find_line="##$NUC2= <1H>" in "../../acqus"|mesh plot (ppm/ppm/intensity)
7|IR spectrum|file_name:"`*.sp`"|x/y plot (energy in nm non-homogeneous scale/intensity)
8|X-ray cristallographic structure|file_name:"*.cif"|3D chemistry structure visualisation)
