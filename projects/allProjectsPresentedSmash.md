# CHEMeDATA projects

Comments and contributions about these tentative projects would be much appreciated. 
## CHEMeDATA-Schema

Introduce **json objects** containing *key data* and *metadata* of common chemistry files in a structured manner.

Examples (tentative):
|file or foler|Key information and metadata|visualizer|standard|
|---|----|---|--|
|.cdx file|molecular formula, INCHI, *etc.*|jsmol|.mol|
|Bruker NMR file folder|Observed nucleus, SNR, *etc.*|nmrium|x/y json|
|etc.||||

 The collection of a set of such **json objects**  will consitute a manifest file, *i.e.* describe the content of an archive files (electronic supplementary information file typically **.ZIP** files submitted as supplementary data at publication or deposition on science repositories.)

Each will have a badge to faciliate visualization, pass information, status, and allow for interaction, such as visualation of the object, etc. 

[![Substance](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/substance.json)](./substance)    [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/sample.json)](./sample)


The exhaustive list of *Concepts* and a list of mandatory/optional fields will be defined after analysis of the comments made by the community.
[See also : ontologies.](../ontologies) [Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)


[More details...](./schema.md)


Schema are not for general chemists to work with, they serve in the background and allow for chemistry-data projects below:
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