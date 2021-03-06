

## Finding chemistry information on the web (Findable)

Locating information using:
- General search tools (google, ...)
- Chemistry database ([chemspinder](https://chemspider.com/), [pubchem](https://pubchem.ncbi.nlm.nih.gov/)
- Specialized database (https://www.ccdc.cam.ac.uk/ for X-ray, etc.)
- Other *finding aids* ...

#### Problem
Except when data are directly submited to a service (such as CCDC for X-Ray structure) these source of information need to identify **new chemistry [Research Object (RO)](http://www.researchobject.org/) on the web**. For example, NMR spectra in the supplementary data of an article need to be identifyable as such (an NMR spectrum) and provide information about the compound it corresponds to. This will allow hummers to catalogue and integrate them.


Tool | Role as solution to the problem
------------ | -------------
*to-be-defined* |  Identify **chemistry** Research Objects (possibly extension of FITS (see below) or as [ro-crate](https://researchobject.github.io/ro-crate/) )
  | ...

## Downloading chemistry information on the web (Accessible)


#### Problem 1
These data typically lack metedata: informations about authors, associated publication, funding agencies, identifyer of the compounds analysed etc. These information are implicitely given by the location of the data, but are about to be lost after the user (or robot)  downloads them to re-use them. Indeed, when a user acess such data only his personal memory makes the link between the data and the source - there is no electronic marks in the files.

Tool | Role as solution to the problem
------------ | -------------
[BagIt](https://en.wikipedia.org/wiki/BagIt) | list content of the archive (no need to read the entire file), insures file integrity (checksum), include metadata about author, etc.
[FITS](https://projects.iq.harvard.edu/fits) | list type of files (.pdf, etc.) Instrument generating the data (for scanned documents), etc. 
  | ...

#### Problem 2
The relationship between the pieces of information are not explicit.
Examples:
- the compound associated to a spectrum is implicit (they may be in the same folder, or in folders with the same name, but this is not easily electronically understanbable.

Tool | Role as solution to the problem
--------- | -------
[NMReDATA](https://nmredata.org) | link NMR spectra to the assignement data and assigned structure

## Opening the files (Reusable/Interoperability)

Chemical informations can be
1. located in a clearly dedicated type of file (.mol, .cif, .jcamp, ...)
2. located in a type of file able to carry different types of data (.sdf, .log, .out, .dat)
3. in a set of multiple files (NMR spectra in Bruker format)
4. just a small section in a the text of thesis, journal article, table in a book, specialized database, wikipedia (melting temperature, IUPAC name, etc.)

#### Problem 
For single-file document (1 and 2) a simple extension of [FITS](https://projects.iq.harvard.edu/fits) may be enough. For more complex data (file trees), additional work has to be done - except if we convert all non-single files RO into single-file RO as part of the standardisation. For example, a Bruker file tree could be converted into a single .jcamp file.

Note: [NIME/chemical](https://en.wikipedia.org/wiki/Chemical_file_format) seem to be abandonned... should it be (re)used?!

### How to indentify them
1. Simple seach of the file extention
2. File extention + additional information in the file (IR/NMR .jcamp file, isotope acquired) 
3. Identify a pattern of files alone (./fid + ./pdata/1/1r + ./acqus + ...procs) possibly need to check in the file to identify isotope
4. Indentify the schema, sentence structure, symbol, etc. of the data in the document

### How to extract specific information 
1. Find, in the file, indication about the exact content: 2D structure, 3D, type of spectroscopy in the .jcamp file 
2. See above. 
3. Get date in the correct file
4. Parse and search for a pattern

### project for diverse chemical information, describe how to find it and caracterize it:

Example 1 chemical structure

Find a chemical structures in a .zip file:
- Search for .mol, .cdx, .sdf files.
- Determine if 2D or 3D
- convert format into "open" format and display (based on MIME chemistry )
https://en.wikipedia.org/wiki/Chemical_file_format#The_Chemical_MIME_Project

Example 2 dihedral angle in a molecule
- Search for .mol, .cdx, .xdf
- Search for 3D structure only
- Extract the angle

### What is needed (IUPAC work)
- List (all the possible) chemical information one may be interested in
- List the criterion to find them (may be provided by manufacturers of instruments...)
- convert them into open format - pack them into .xml ?
- display them to human.
 
### Semantic and definition ? 

#### 1D 1H NMR spectrum:
1) is a "1D NMR spectrum"
2) is a 1H detected isotope (nucl in .acqus file)
#### 1D NMR spectrum:
1) is a "NMR spectrum"
2) is a 1D spectrum (presence of acqu2s file)
#### NMR spectrum:
1) includes ./acqus + (./fid or .ser) + ./pdata/**N**/1r OR 

XML too vague.
More specific may come from:
- [OWL](https://www.w3.org/OWL/) for visualisation see below (vowl)
- [vowl](http://vowl.visualdataweb.org/) part of [w3](https://www.w3.org/standards/about.html) (is this relevant in chemistry !?) [see this...](http://vowl.visualdataweb.org/webvowl.html)
- [RDF](https://www.w3.org/2001/sw/wiki/RDF)
- [DOI shema](https://www.doi.org/doi_handbook/DOI_Schema_Release_Notes.html)

Entity Relationship Diagram (
E-R Diagram [example](https://creately.com/diagram/example/h7cw0wrb1/%20E-R%20Diagram%20of%20Library%20Management%20System) )  

USE CASES approach for involving others!! 
KEY CONCEPT: Finding pieces (RO) in .zip files (or elsewhere)

Relevant to our work:
Electronic lab books because the ata in lab books make the link between RO. Example at [KIT](https://www.chemotion-repository.net/welcome).

Level of processing:
- in NMR (fid, xf2 data, xfb data - FID, series of spectra, 2D spectra...)
- with NASA data 
- CERN data also level of processing.
