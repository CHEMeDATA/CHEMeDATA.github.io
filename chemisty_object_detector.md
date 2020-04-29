# Chemistry object 

## Perpective

We describe here to describe the content of a zip file including chemical data found in repositories such as Zenodo, University archive, suplementary information pages of jounals, *etc*.

Repository service typically use [FITS](https://projects.iq.harvard.edu/fits/home) providing information about the files. [FITS](https://projects.iq.harvard.edu/fits/home) identifies  image, spreadsheets, the type of .pdf, *etc*. But this method does not recognize the files commonly used in the specialized field of chemistry. 

## Listing chemistry objects

Listing chemical structures, NMR spectra, *etc.* would allow the visitor to:
 - visualize the chemical structures,
 - have a look at an NMR spectrum, or the assignment data
 
whithoug having to download the entire archive. 
He could be be able to download only the part of interest.
 
In order to be able to list chemical structures, NMR spectra, *etc.* criteria need to be listed to identify them. A method aiming at identifying the [Chemistry Objects](chemisty_object.md) found in an archive file (.zip) is the object of the ["Chemistry research object identification"](https://chemedata.github.io/ResearchObjectFinder/). In short, the procedure consists in searching, in each folder of the archive, for a specific file name, or a pattern of files and fulfil additional criteria (see "Short list" Table). 

<!--- For .zip files one may need to extract the list of the files. For [BagIt](https://en.wikipedia.org/wiki/BagIt) archive, reading a manifest should be enough, provided it is easily acessible from the portail. The manifest (manifest-XXX.txt where XXX is md5, sha1, *etc.*) is one of the *tags* (metadata about the *payload*) of the *bag*. --->

## Giving chemistry objects flesh and blood

Allowing to extact part of an archived makes the loss of context possible problematic downstream, when the the researcher will need to refer to the source of the data, or find related information later on. The donwloaded "chemistry objects" could include additional information (for example, the chemical shifts for each carbon) with the 3D structure of the compound. It should also carry with it, metadata about its origin, how to cite the work, its INCHI (to faciliate search of additional information about the compound, etc.)

## Short list of Chemistry object
This is just a short list for illustration purpose. More info can be found in the ["Chemistry research object identification"](https://chemedata.github.io/ResearchObjectFinder/) project.

<!---  of a [longer list](#long-list-of-chemistry-object) (see below) providing more complex examples. --->

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

