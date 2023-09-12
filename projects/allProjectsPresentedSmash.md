# CHEMeDATA projects

Comments and contributions about these tentative projects would be much appreciated. 


See also : [ontologies](../ontologies). 
[Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)



## CHEMeDATA-Schema

Goal: 

Produce general chemistry schema-based data description of chemistry data files. This project will define the structure of **json objects** describing the content of .mol files, of Bruker nmr spectra, *etc.* They will include the *key data* and *metadata* of common chemistry files in a structured manner. The collection of a set of such **json objects**  will consitute a manifest file, *i.e.* describe the content of an archive files (electronic supplementary information file typically submitted as supplementary data at publication or deposition on science repositories.)

The CHEMeDATA-Schema formalism has three layers detailed below.
- 1 Concepts
- 2 Key types
- 3 Derived types

### CHEMeDATA-Schema/Concepts

Schema for key chemical concepts called CHEMeDATA-Schema/Concepts: (Sample, transformation, analytics...). See ... for more details.

	- Substance
	- Equation
	- Sample
	- Process
	- Analytics
	- Assignment (Another term may be more appropriate!)


Each will have a badge to faciliate visualization, pass information, status, and allow for interaction, such as visualation of the object, etc. 

[![Substance](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/substance.json)](./substance)    [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/sample.json)](./sample)


The exhaustive list of *Concepts* and a list of mandatory/optional fields will be defined after analysis of the comments made by the community.
[See also : ontologies.](../ontologies) [Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)


### CHEMeDATA-Schema/Types

The *types* will specify the type of (say) **sample**. There will be a list of schema for instances chemical Concepts.


Example: Solvent* (is simply a type of Compound* at the liquid state. It will be used for the description of liquid-state Sample*)

Example: structure3Dmol* (Compound* in a mol file)

Example: compound3D* (compound with an inchi, a compound name and a structure3Dmol*)

Examples: simpleSolutionSample (a ChemE-Type) is a type of "Sample" (a ChemE-Concept see ChemE-Concepts).


"ChemE-type" : "solution sample",
"ChemE-Concepts" : "sample"
"author/company/institution..." To be discussed. Who would introduced concepts? Software companies, adademic instituation or research group? Academies? Societies?
Required-fields : [
	solvent : "ChemE-Solvent"
	deuterated : "Yes, no, partial"
	deuterationLevel : "
]
#### Key Types

The key types will be defined by at the initial stage of the introduction of CHEMeDATA-Schema in order to provide a general and broad basis. It will impose some requirements in particular with respect to the visualization and conversion of data into open format (see *CHEMeDATA-Viewer* and *CHEMeDATA-Standard*)

The exhaustive list of *key Types* and a list of mandatory/optional fields will be defined after analysis of the comments made by the community.

Examples of possible *key types*: 

- the CHEMeDATA-Schema/equation/oxydation: 

[![Oxidation](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/equation2Ox.json)](./equation) 

- the CHEMeDATA-Schema/analytics/spectroscopy/nmr: 

[![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/analysisNMRspectra.json)](./analysis/NMR)


[Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)
#### Derived Types

We want to allow anybody to introduce derived types. This will allow to refine the description of the existing types. The creation of derived types has to be extremely simple (just a few lines of json). 
Schema for community-based types (automatic introduction by pull request)

[Illustration of derivation](./derivation)

Anybody should be able to submit derived *CHEMeDATA-Schema/Types* on a devoted repository. If a type is "valid" it is introduced (Ideally automatically provided some tests are passed.). The pertinence is not judged (?), it is the responsability of the person who commits the data.

Example of a possible *Derived types*: 

[![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/assignmentNMRspectra.json)](./assignment/NMR)

[![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/assignmentNMRdata.json)](./assignment/NMR) 

[Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)
### CHEMeDATA-Viewer

This project will define a list of validated visualizers of the *Key CHEMeDATA-Schema/Types*.

Examples of visualization: 
- the 3D structures of compounds
- *flat* 2D structures of organic compounds
- 1D NMR spectra
- *etc.*

See also *CHEMeDATA-Standard*.

### CHEMeDATA-Standard

This project will define a list of standard file format for the *Key CHEMeDATA-Schema/Types*.

The role of a standard for the Key types is to facilitate the visualization. For example, many file format code 3D structures of organic compounds. Having a defined standard allows the visualizer to rely on a stable basis to visualize all 3D structures. If a new format is introduced, the integration in the CHEMeDATA world only requires the author provide a converter to a unique default format.

See also *CHEMeDATA-Viewer*.

## CHEMeDATA-Archeology

Automatize the extraction of chemical information from publication, thesis. 

Goal, make chemical data more searchable.

Input: Article, thesis in pdf format

Output: extracted data in the CHEMeDATA schema format.

## CHEMeDATA-Release

### *Goal*
Make collections of chemistry data public. Whether they are personal, institutional, or industrial collections of chemistry data may require processing, filtering, anonymization, before they can be made public. The project will propose services and tools to facilitated the publication of collections of NMR spectra in a legal manner - this is not a CHEMeDATA-leaks project. 

**Audience**: Curators of NMR spectra collections, quality control managers in chemical compound production, *etc.*

**Help needed**: Python developper (A language avoiding compilation, clearly showing the code of the processing and avoiding a browser should reassure the user that data are not leaking but under the tight control speak in favor of python.)



### Examples of extracted data

The list of carbon chemical shifts for a compound described in a paper

```json
CompoundWithNMRshift:{
	"reference": {
		"doi": "... doi of the source",
	},
	"extraction": {
		"... information about the method of extraction of the data (manual... software... author...)"
	},
	"compound":{
		"inchi": "inchi of the compound generated during extraction.",
		"inchiKey": "inchiKey of the compound generated during extraction. ?Needed?",
		"name": "the name of the compound used in the paper/thesis"
		},
	"NMRdata": {
		"nucleus": "1H",
		listChemicalShift : [23.3, 45.9]
	}
}
```

A schema of CompoundWithNMRshift will insure consistent format and content of the data. It could make the inchi or the solvent mandatory, but if a data extractor is not capable to fulfill the requirement, it could introduce a CompoundWithNMRshift_Light scheme that would not impose the requirement. 

Logo: pinceau, pioche molecules loupe

# Posters

## Projects

## We need you!

Do you have data?