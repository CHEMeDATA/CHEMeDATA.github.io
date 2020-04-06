# Introduction
There is no clear or autoritarian definition of a chemistry object (CO). 

In this context it refers to any piece of information relevant to chemistry. 
- the structure of a compound (drawing, .xcd file, flat representation or 3D representation, etc.)
- the output of a computer program of scientic instrument (spectrum, list of the energy of molecular orbitals, etc)
- the crude result from a scientific instrument
- the interpreted results of an experiment 

The word [*object*](object.md) has a special meaning in computer sciences indicating that it has an electronic form meaning that it is computer understandable. A .jpg image of a spectrum, for example, cannot be understood by a computer to be a spectrum. It is an *image* object, not a chemistry or spectrum object. 
# Ontology of chemistry object
An ontology of chemistry objects should be proposed by the chemistry community.
Examples: 
 - spectrum (generic)
   - NMR spectrum 
     - 1D NMR spectrum (image, jcamp, Spectrometer data)
     - 2D NMR spectrum (image, jcamp, Spectrometer data)
 - Full NMR analysis (including a set of spectra of different nature of the same sample) **this may be simply a [collection](https://schema.org/Collection) of spectra**
 - series of spectra (diff temp, diff concentration of ligand...) **this not just a set of spectra, the varied parameter has to be documented**
 - chemical structure
   - 2D (mol, cdx, etc.)
   - 3D (mol, ...)
 - chemical reaction (includes chemical strucutres and conditions... see ....)
 - data
   - single data (Example: the mass of an element)
   - array of data **this may be simply a set of spectra** 
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
