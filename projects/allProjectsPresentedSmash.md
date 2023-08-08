# All projects

## CHEMeDATA-Schema

### CHEMeDATA-Schema/Concepts

Schema for key chemical concepts (Sample, transformation, analytics...). See ... for more details.

```json
"ChemE-Concepts" : ["sample",
"transformation",
"ADDDDD THE OTHERS"
]
```

The exhaustive list of Concepts and a list of mandatory/optional fields is defined by a pannel of experts during the elaboration of ChemE-Concepts.

### CHEMeDATA-Schema/Types

Schema for instances chemical instances on the ChemE-Concepts.

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

Schema types validated by the CHEMeDATA pannel. The key types may need to fullfil requirements, for example have an existing visualizer.

#### Derived Types

Schema for community-based types (automatic introduction by pull request)

The community submit "ChemE-Types" on a repository. If a type is "valid" it is introduced. The pertinence is not judged (?), it is the responsability of the person who commits the data.

### CHEMeDATA-Schema/View

Schema for the visualization of CHEMeDATA-Schema/Types. 

Example: visualization of the 3D structure of a compound, visualization of an NMR spectrum.

name : js-view??
url : "http.... point to the visualization tool"
compatibility : [type: molecu]


Example: visualization of a 

## ChemE-Archeology

Automatize the extraction of chemical information from publication, thesis. 

Goal, make chemical data more searchable.

Input: Article, thesis in pdf format

Output: extracted data in the CHEMeDATA schema format.

## ChemE-Leaks

Make collections of chemistry data public. Whether they are personal, institutional, industrial collections may require processing, filtering, annonimization, before they can be made public. The project will propose services and tools to facilitated the publication of collections of NMR spectra in a legal manner (unlike what the name of the project may ). 

Audience: institution with collection of NMR spectra, chemical componds producers with quality control including NMR, etc.



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