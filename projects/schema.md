

## CHEMeDATA-Schema

The goal is to produce general chemistry schema-based data description of chemistry data files. This project will define the structure of **json objects** describing the content of chemistry files.


The CHEMeDATA-Schema formalism has three layers detailed below.
- 1 Concepts
- 2 Key types
- 3 Derived types

See also : [ontologies](../ontologies). 
[Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)
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