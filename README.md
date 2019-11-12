# CHEMeDATA.github.io
main website of the CHEMeDATA ombrella organization 

### Goal
Make chemical information available

### List of supports of chemical information

Chemical informations can be
1. located in a clearly dedicated type of file (.mol, .cif, .jcamp, ...)
2. located in a type of file able to carry different types of data (.sdf, .log, .out, .dat)
3. in a set of multiple files (NMR spectra in Bruker format)
4. just a small section in a the text of thesis, journal article, table in a book, specialized database, wikipedia (melting temperature, IUPAC name, etc.)

### How to indentify them
1. Simple seach of the file extention
2. File extention + additional information in the file (IR/NMR .jcamp file, isotope acquired) 
3. Identify a pattern of files alone (./fid + ./pdata/1/1r + ./acqus + ...procs) possibly need to check in the file to identify isotope
4. Indentify the schema, sentence structure, symbol, etc. of the data in the document

### How to extract specific information 
1,2. Find, in the file, indication about the exact content: 2D structure, 3D, type of spectroscopy in the .jcamp file 
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

### What is needed ? 
- List (all the possible) chemical information one may be interested in
- List the criterion to find them
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
