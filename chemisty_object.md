# Forwords

There is no clear or autoritarian definition of a chemistry object (CO) or mappin into any specific ontology. This may come at the later stage (and a few words are mentionned below). 

It is currently based on a use-case needs, in particular the need to ["indentify"](https://chemedata.github.io/ResearchObjectFinder/) chemistry *stuff* from archived chemistry data stored in .zip files. 

## Digital Objects
 - FairSpec digital.finding.aid Object
     - Properties:
 
### Compound (Meta)Data
  - FairSpec chemical.identifier.metadata Object
     - Properties:
        - Inchi
        - Formula(s)
        - SMILE(s) 
        - Meltng Point
        - [selected spectroscopy extracted data]
  - 2D SDF Object(s)
  - 3D SDF Object(s)
  - Computational Results Object(s)
  - Experimental Procedure()
  
### Spectroscopy Data
  - FairSpec spectroscopy.data.metadata Object
     - Properties:
  - Vendor-Specific Digital Object(s)
  - JDX Digital Object(s)
  - Spectrum PDF Object
  - Spectrum image Object

### Assignment Data
  - FairSpec assignment.data.metadata Object
     - Properties:
  - NMReData Object
  - Spinus Analysis Object
  - NMRDB Object

## Digital Entities
  - Additional Uncatalogued Digital Entities
  
  
# TODO: Map these ideas to the above

## Chemistry objects
This is a tentative list of objects and relations.
### Compound
  - Types
    - Formula
    - 2D structure in file (.mol .cdx .dcxml)
    - 3D mol file (.mol .out from gaussian09, *etc.*)
    - image of any of the above
  - Properties
    - Has a formula (always)
    - Has an INCHI (always)
    - Has a list of atoms (always can it be explicit? Always?  Even for diastereotopic H of structure with implicit H?)
    - Has a list of bonds (always ? from mol file? or from xray for structure in solid?)
    - Has an origin link to (article, thesis, website communication, database, ? // with DOI ?)
    - Has an reference into to above-mentionned (article, thesis, website communication, database, ? // with DOI ?) For example compound 1.
    - Is shown in Figure... into to above-mentionned (article, thesis, website communication, database, ? // with DOI ?) For example compound 1.
    - Is mentionned at page ... into to above-mentionned (article, thesis, website communication, database, ? // with DOI ?) For example compound 1.
    - Characterization (NMR, MS, etc... )
        - has predicted chemical shifts? Is this embedded chemical property?
        - has chemical shifts
          - has assigned chemical shifts ? (for visualization...)
          - just text of chemical shifts?
        - has experimental J-coupling constants ? (for visualization...)
      - explicit link to atoms of the molecules canonical numbering of H and C?
    - NMR characterization - is this part of the compound properties - make the reciprocal link to the assignment (see below)? 
###  Chemical property, spectra, etc.
  - Types
    - Melting point
    - NMR spectrum (the post processing part)
    - NMR experiment (the pre processing part)
    - IR spectrum 
    - Image of the spectrum
  - Properties
    - From:to x_axis (for all spectra)
    - From:to additional dimension in 2D NMR (not always)
    - Units (for each dimension) (always)
    - peaks (not always) peak may have additional features... coupling structures, etc.
    - for NMR, essential property is Larmor....
    - Assignment
  - metadata 
    - instrument, date of acquisition )
    - Associated publication ? (is this part of the spectrum property - make reciprocal link to the publication)
    - Associated compound ? (is this part of the spectrum property - make reciprocal link to the assignment)
###  Assignment 
Only necessary if includes some detail - if just to say "this spectrum corresponds to this molecule", link may be in the spectrum/compound object ?? Or always, because this is a link
  - Properties
    - has one (or more - if mixture) molecules
      - just link to .mol file?
    - has one or more spectra.
      - just link to spectrum object file?
    - Collection of links of:
      - Property of spectrum (peak) to a property of Compound (atom for NMR - bound for IR - fragment for MS)
    - metadata 
      - date?
      - computer/algo/operator?
      - correction/addition to other assignemnt?

A full NMReDATA records could create:
- one molecule(or more if mixture) 
- one spectrum per spectrum mentionned in the NMR record, and 
- one/multiple assignment ? (one per spectrum, one for the whole NMR - one for all analitics of a compound?)

NMReDATA includes multiple ontologies:
-The core assignment (chemical shift and coupling (agregated) linked to atom number in molecule.
-ontology of single-spectrum description
-ontology of a 1D signal
-ontology of a 2D signal


In this context it refers to any piece of information relevant to chemistry. 
- the structure of a compound (drawing, .xcd file, flat representation or 3D representation, etc.)
- the output of a computer program of scientic instrument (spectrum, list of the energy of molecular orbitals, etc)
- the crude result from a scientific instrument
- the interpreted results of an experiment 

The word [*object*](object.md) has a special meaning in computer sciences indicating that it has an electronic form meaning that it is computer understandable. A .jpg image of a spectrum, for example, cannot be understood by a computer to be a spectrum. It is an *image* object, not a chemistry or spectrum object. 

# Ontology of chemistry object

Objects will have [schema](https://schema.org/) representation.
We would probably use RDF to link elements (part of a OWL ontology).

Prelimary list of chemistry objects (to be refiined by the chemistry community):
 - Chemical structure
   - 2D (mol, cdx, etc.)
   - 3D (mol, ...)
 - Chemical reaction (includes chemical structure of the reactants and products and conditions... see ....)
 - Chemical property
   - Single data (Example: the mass of an element : A<sub>r,std</sub>(Y) = 88.90584.
   - Array of data **this may simply a [collection](https://schema.org/Collection) of** ***single data***. 
 - Spectrum (generic)
   - NMR spectrum (subcategory of *spectrum*)
     - 1D NMR spectrum (image, jcamp, Spectrometer data)
     - 2D NMR spectrum (image, jcamp, Spectrometer data)
 - Full NMR analysis (including a set of spectra of different nature of the same sample) **this may be simply a [collection](https://schema.org/Collection) of spectra**
 - series of spectra (diff temp, diff concentration of ligand...) **this not just a set of spectra, the varied parameter has to be documented**

 - NMR assignment (NMReDATA, "ACS assignment text")
Existing schema the should be integrated:
 - [author](https://schema.org/Person)
 - reference to article/book section
 - reference to institution
 - funding agencies
 - funding agencies
 
For each type of object, we should state which property is mandatory/optional.
Consider if we should have out own schema (in hirited from "official" ones - with [XSLT](https://en.wikipedia.org/wiki/XSLT) .
Each main schema should have flavors (in parenthesis)
...

Set of objects will use existing schema
# Use cases
## chemistry data in ZIP files
By nature, the XML format allows to combine the XML of a set of objects. For .zip file including chemistry files the list of objects should be included a manifest file (say chemObjmanifest.xml) listing all the identified objects included in the file with a link to each file.
## chemistry objects uploaded from database
When chemist download data (say a spectrum, a chemical structure, etc) a manifest file could be associated to the object (in the zip file including the paylowad) If the file is dowloaded "alone" the metadate about the object could be included in the file (for jcamp, one could include fields corresponding to the metadate of the object - origin, in particular- Pdf also allows to include metadata). Even more general, an alternative would be for database to calculated the .md5 of all downloadable files (spectra, mol files, etc.) and have a registry of files so that the origin of a file could be retraced back using a RESTfull-API or a centralized service (datacite ?) to offers such a service.



## Key aspects

- Ability of humans to understand and determine the context of the occurance of the object
- Ability of a computer to identify the object and put it in relation to others objects or other relevant information (author, date of publication, etc.)

Eg. A hand-made drawing is not "readable" by a computer program, a .cdx is readable by commercial software, .mol files can be read my multiple type of free sofware and web tools.

## Relevance 

The (chemistry) objects carry information that can be seached for used by 
- humans to be learned, taught, cited, or used in other ways
- computers to be integrated into database, or any used in any type of processing.

Facilited the *use* is the key aspect of open and [FAIR](https://www.go-fair.org/fair-principles/) data.


**Note:** that [Research Object](https://researchobject.github.io/ro-crate/) (RO) has no relevance to the specifically chemical ontology presented here.
