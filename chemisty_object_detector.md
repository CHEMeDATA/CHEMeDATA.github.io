# Chemistry object detector 

We describe here a method aiming at listing the [Chemistry Objects](chemisty_object.md) found in an archive file (.zip, BagIt, etc.).

The procedure consists in searching, in each folder of the archive, for a specific file name or a pattern of files 
and fulfil additional criteria (see "Short list" Table).

Perspective: Develop methods to allow visitor of a repository to direclty visualize the Chemistry Objects listed for a given record. This will require to develop a resource providing a automated mecanism (API) to visualize the chemistry objects. 

[Example of a pop-up of a 2D molecular structure](https://www.simolecule.com/cdkdepict/depict/bow/svg?smi=indole%0A%20%20NextMove10101914192D%0A%0A%20%209%2010%20%200%20%200%20%200%20%200%20%200%20%200%20%200%20%200999%20V2000%0A%20%20%20%201.7200%20%20%20-1.2100%20%20%20%200.0000%20N%20%20%200%20%200%0A%20%20%20%202.6000%20%20%20-0.0000%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20%201.7200%20%20%20%201.2100%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20%200.2900%20%20%20%200.7500%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20-1.0100%20%20%20%201.5000%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20-2.3100%20%20%20%200.7500%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20-2.3100%20%20%20-0.7500%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20-1.0100%20%20%20-1.5000%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20%200.2900%20%20%20-0.7500%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%201%20%202%20%201%20%200%0A%20%202%20%203%20%202%20%200%0A%20%203%20%204%20%201%20%200%0A%20%204%20%205%20%202%20%200%0A%20%205%20%206%20%201%20%200%0A%20%206%20%207%20%202%20%200%0A%20%207%20%208%20%201%20%200%0A%20%208%20%209%20%202%20%200%0A%20%201%20%209%20%201%20%200%0A%20%204%20%209%20%201%20%200%0AM%20%20END%0A) using [cdkdepict](https://www.simolecule.com/cdkdepict/depict.html).  

<script type="text/javascript" src="https://chemapps.stolaf.edu/jmol/jmol.php?smi=indole%0A%20%20NextMove10101914192D%0A%0A%20%209%2010%20%200%20%200%20%200%20%200%20%200%20%200%20%200%20%200999%20V2000%0A%20%20%20%201.7200%20%20%20-1.2100%20%20%20%200.0000%20N%20%20%200%20%200%0A%20%20%20%202.6000%20%20%20-0.0000%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20%201.7200%20%20%20%201.2100%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20%200.2900%20%20%20%200.7500%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20-1.0100%20%20%20%201.5000%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20-2.3100%20%20%20%200.7500%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20-2.3100%20%20%20-0.7500%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20-1.0100%20%20%20-1.5000%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%20%20%200.2900%20%20%20-0.7500%20%20%20%200.0000%20C%20%20%200%20%200%0A%20%201%20%202%20%201%20%200%0A%20%202%20%203%20%202%20%200%0A%20%203%20%204%20%201%20%200%0A%20%204%20%205%20%202%20%200%0A%20%205%20%206%20%201%20%200%0A%20%206%20%207%20%202%20%200%0A%20%207%20%208%20%201%20%200%0A%20%208%20%209%20%202%20%200%0A%20%201%20%209%20%201%20%200%0A%20%204%20%209%20%201%20%200%0AM%20%20END%0A&link=Example of pop-up of a 3D structure"></script> using [JSmol](http://wiki.jmol.org/index.php/Main_Page).


## Short list of Chemistry object
This is a short version of a [longer list](#long-list-of-chemistry-object)(see below) providing more complex examples.

#|Chemistry object | Criteria | Type of data |visualization
-|------|---|---|--
2|Bruker 1D <sup>1</sup>H NMR spectrum|file_name=="`1r`" & exist_file:"`../../fid`" & exist_file:"`../../acqus`" & find_line="##$NUC1= <1H>" in "`../../acqus`"|x/y plot (ppm/intensity)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
7|IR spectrum|file_name=="`*.sp`"|x/y plot (energy in nm non-homogeneous scale/intensity)|[JCAMP-DX](http://jcamp-dx.org/), simple x/y plot
8|X-ray crystallography structure|file_name=="`*.cif`"|3D chemistry structure visualization)|[JSmol](http://wiki.jmol.org/index.php/Main_Page), etc.
9|2D molecular structure|file_name=="`*.cdx`"|2D chemistry structure visualization)|[JSmol](http://wiki.jmol.org/index.php/Main_Page), etc. after conversion!

Examples of the above-mentionned objects can be found in the files:
```
/researchdata/NMR Files per compound/3r_(R)-Me-FBn-18C6/2/pdata/1/1r
/researchdata/Other Data per compound/3n_(S)-Me-1-naphth-18C6/3n_X-Ray/3n_(S)-Me-1-naphth-18C6-NaBArF.cif
/researchdata/Other Data per compound/3n_(S)-Me-1-naphth-18C6/2nd eluted/3n_(S)-Me-1-naphth-18C6_2nd elt_FT-IR.sp 
/researchdata/Other Data per compound/3n_(S)-Me-1-naphth-18C6/3n_(S)-Me-1-naphth-18C6.cdx
```
from this [yareta record](https://yareta.unige.ch/frontend/archive/62c9dc3b-6f44-4b3b-963d-1ab31c17f6c6). 

The criteria (third column in the table) are discussed [below](#criteria). 

# Criteria
We defined three test/functions:
- file_name (test presence of file)
- exist_file (test presence of additional files)
- find_line (test presence of a string in a text file)

See below for more details.
## File name
In the simplest cases, the only criterion is the presence of a specific file (file_name=="`1r`") or filename extention (file_name=="`*.sp`"). 
## Presence of associated files
In some cases, the presence of additional files has to be tested.
This is done with: 
```
exist_file:"./procs" 
exist_file:"../../acqus" 
exist_file:"../../fid" 
```
Note that associated files may be in a separate folder (see the path before the file name). The locations are relative to the reference file (see above).
## Presence of a specific string in a file
Additional conditions may be necessary to refine the identification. For example the presence of a magic key or other [file signature](https://en.wikipedia.org/wiki/List_of_file_signatures). This can be used to test the value for a parameter. For example: 
```
find_line="##$NUC1= <13C>" in "`../../acqus`
```
means that a given string of characters if found in a give file.

This allows to distinguish different (sub)types of objects. Inthis specific case, to disthinguish a 1D <sup>13</sup>C NMR spectra from 1D spectra of other isotope). We need to make this distinction to make a precise list of the content of the archive.

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
8|X-ray crystallography structure|file_name=="`*.cif`"|3D chemistry structure visualization)|[JSmol](http://wiki.jmol.org/index.php/Main_Page), etc.
9|2D molecular structure|file_name=="`*.cdx`"|2D chemistry structure visualization)|[JSmol](http://wiki.jmol.org/index.php/Main_Page), etc. after conversion!
10|2D molecular structure|file_name=="`*.mol`" & presence of "2D" at specific location in the file|2D chemistry structure visualization)|[JSmol](http://wiki.jmol.org/index.php/Main_Page), etc.
11|3D molecular structure|file_name=="`*.mol`"  & presence of "3D" at specific location in the file|3D chemistry structure visualization)|[JSmol](http://wiki.jmol.org/index.php/Main_Page), etc.

The list of examples is quite preliminary and (purposively) uneven and (in some cases incomplete). The aim is only to show the underlying ontology which should be defined (possibly using [OWL](https://www.w3.org/TR/owl2-primer/)?).
