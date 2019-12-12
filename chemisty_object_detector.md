# Chemistry object detector 

We describe here a method aiming at listing the [chemistry objects](chemisty_object.md) found in an archive file (.zip, BagIt, etc.).

The procedure consists in searching in each folder of the archive for a specific file name of pattern of files 
and (sometime) fulfil additional criteria. 

## Short list of Chemistry object
This is a short version of a [longer list](#long-list-of-chemistry-object) providing more complex examples.

#|Chemistry object | Criteria | Type of data |visualization
-|------|---|---|--
2|Bruker 1D NMR spectrum (generic)|file_name=="`1r`" & exist_file:"`../../fid`" & exist_file:"`../../acqus`"|x/y plot (ppm/intensity)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
7|IR spectrum|file_name=="`*.sp`"|x/y plot (energy in nm non-homogeneous scale/intensity)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
8|X-ray crystallography structure|file_name=="`*.cif`"|3D chemistry structure visualization)|[JSmol](https://atom.calpoly.edu/viewer/), etc.

Examples originate from [yareta record](https://yareta.unige.ch/frontend/archive/62c9dc3b-6f44-4b3b-963d-1ab31c17f6c6) files:
```
/researchdata/NMR Files per compound/3r_(R)-Me-FBn-18C6/2/pdata/1/1r
/researchdata/Other Data per compound/3n_(S)-Me-1-naphth-18C6/3n_X-Ray/3n_(S)-Me-1-naphth-18C6-NaBArF.cif
/researchdata/Other Data per compound//3n_(S)-Me-1-naphth-18C6/2nd eluted/3n_(S)-Me-1-naphth-18C6_2nd elt_FT-IR.sp 
```
The criteria (third column) are discussed [below](#criteria). The list is quite preliminary and (purposively) uneven and (in some cases incomplete). The aim is only to show the underlying ontology which should be defined (possibly using [OWL](https://www.w3.org/TR/owl2-primer/)?).

# Criteria
## File name
In the simplest cases, the only criterion is the presence of a specific file (file_name=="`1r`") or filename extention (file_name=="`*.sp`"). 
## Presence of associated files
In some cases, we want to test the presence of additional files in the same or other folders relative to the main file.
For example: 
```
exist_file:"./procs" 
exist_file:"../../acqus" 
exist_file:"../../fid" 
```
Note that associated files may be in a separate folder. The location is relative to the reference file (file_name).
## Presence of a specific string in a file
Additional conditions may be necessary such as the presence of a magic key (or other [file signature](https://en.wikipedia.org/wiki/List_of_file_signatures)). This can be used to test the value for a parameter. For example: 
```
find_line="##$NUC1= <13C>" in "`../../acqus`
```
means that a file located at the given position relative to the main file (see above).
This allows to distinguish different type of objects. (here a <sup>13</sup>C 1D from other NMR spectra).


## Long list of Chemistry object

#|Chemistry object | Criteria | Type of visualization
-|------|---|---
1|Bruker 1D NMR FID|file_name:"fid" & exist_file:"`./acqus`"|x/y plot (time/intensity)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
2|Bruker 1D NMR spectrum (generic)|C1=[file_name=="1r" & exist_file:"../../fid" & exist_file:"../../acqus"]|x/y plot (ppm/intensity)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
3|Bruker 1D <sup>1</sup>H NMR spectrum|C1 & find_line="##$NUC1= <1H>" in "`../../acqus`"|x/y plot (<sup>1</sup>H ppm/intensity/integrals)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
4|Bruker 1D <sup>13</sup>C NMR spectrum|C1 & find_line="##$NUC1= <13C>" in "`../../acqus`"|x/y plot (<sup>1</sup>1H ppm/intensity/peak picking)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
5|Bruker 2D NMR spectrum(generic)|C2=[file_name=="2rr" & exist_file:"../../ser" & exist_file:"`../../acqus`" & & exist_file:"`../../acqu2s`"]|mesh plot (ppm/ppm/intensity)|[2D JCAMP-DX](http://jcamp-dx.org/), ??
6|Bruker 2D NMR HSQC spectrum|C2 & find_line="##$NUC1= <13C>" in "../../acqus" & find_line="##$NUC2= <1H>" in "`../../acqus`"|mesh plot (ppm/ppm/intensity)|[2D JCAMP-DX](http://jcamp-dx.org/), ??
7|IR spectrum|file_name=="`*.sp`"|x/y plot (energy in nm non-homogeneous scale/intensity)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
8|X-ray crystallography structure|file_name=="`*.cif`"|3D chemistry structure visualization)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
