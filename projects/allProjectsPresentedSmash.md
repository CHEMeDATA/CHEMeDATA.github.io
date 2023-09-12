# CHEMeDATA projects

Here is a tentative list of projects presented at the Smash conference 2023. It should be considered as *Work in progress!* which will evolve depending on the interest expressed by the visitors of our booth. Note that is, currently completely non-profit activity. 

Some projects may be developed with industrial partners and public funding agencies, notably the PANACEA project involving Mestrelab, but anything called CHEMeDATA will remain an "open" initiative with MIT licensing.

## CHEMeDATA-Schema

We introduce **json objects** to contain *key data* and *metadata* of common chemistry files in a structured manner.

Tentative examples:

|file or foler|Key information and metadata|visualizer|standard|
|---|----|---|--|
|.cdx file|molecular formula, INCHI code, *etc.*|jsmol|.mol|
|Bruker NMR file folder|Observed nucleus, SNR, *etc.*|nmrium|x/y json|
|etc.||||


Each **json objects** will have a badge to faciliate identification, pass a status and allow for interaction, such as visualation of the object, *etc.*

[![Substance](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/substance.json)](./substance) 

A collection of **json objects**  will constitute a manifest file, *i.e.* describe the content of an archive files, typically a **.ZIP** files of "electronic supplementary information" submitted with articles for publication or deposited on science repositories such as figshare, Zenodo, *etc.*

[More details...](./schema.md)

**Note:** Schema are not for general chemists to work with, they serve in the background and allow for chemistry-data projects below:

### CHEMeDATA-Finder

Crowling the web in the search of data. With the manifest, much easier...

Repository of certified CHEMeDATA?
Findability is essential ....
### CHEMeDATA-Viewer

This project will define a list of validated visualizers of the *Key CHEMeDATA-Schema/Types*.

Examples of visualization: 
- the 3D structures of compounds
- *flat* 2D structures of organic compounds
- 1D NMR spectra
- *etc.*

See also *CHEMeDATA-Standard*.

Why do this? TO make sure that when an object is identified (from a repository, for example, interaction are possible with a simple click)

### CHEMeDATA-Standard

This project will define a list of standard file format for the *Key CHEMeDATA-Schema/Types*.

The role of a standard for the *Key Types* is to facilitate the visualization of chemistry data. For example, many file format code 3D structures of organic compounds. Having a defined standard allows the visualizers to rely on a stable basis to visualize any 3D structures. If a new format is introduced, the integration in the CHEMeDATA world only requires the author provide a converter to a single format.

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

**Help needed**: Python developer (A language avoiding compilation, clearly showing the code of the processing and avoiding a browser should reassure the user that data are not leaking and remain under the tight control...speaks in favor of python. Could be argued, for sure!)



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