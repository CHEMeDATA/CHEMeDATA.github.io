# CHEMeDATA projects

Here is a tentative list of projects presented at the Smash conference 2023 in Baveno, Italy. It should be considered as a *Work in progress!*. It will evolve depending on the interest expressed by the community, starting with the visitors of our booth.
## CHEMeDATA-Schema

We introduce **json objects** to contain *key data* and *metadata* of common chemistry files in a structured manner.

Tentative examples:

|file or folder|Key information and metadata generated|CHEMeDATA-Visualizer|CHEMeDATA-Standard|
|---|----|---|--|
|.cdx/.cdxml file with a single compound|molecular formula, INCHI code, *etc.*|jsmol|.mol|
|Bruker NMR file folder|Observed nucleus, SNR, *etc.*|nmrium|x/y json|
|etc.||||

Each **json objects** will have a badge to facilitate identification, pass a status and allow for interaction, such as visualation of the object, *etc.*

[![Substance](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/substance.json)](./substance) 

A collection of **json objects**  will constitute a manifest file describing the content of an archive files, typically a **.ZIP** files of "electronic supplementary information" submitted with articles for publication or deposited on science repositories such as figshare, Zenodo, *etc.*

[More details...](./schema.md)

**Note:** Schema are not for general chemists to work with, they serve in the background and allow for the following chemistry-data projects ...
### CHEMeDATA-Finder

Finding chemical information is notoriously difficult. Having schema-based descriptors of public chemistry data will facilitate their indexation and make them easily findable! For example, the presence of the NMR spectrum of menthol in the archive file of indexed data repositories would be trivially findable by search engines.

Help needed:
- Develop a CHEMeDATA-Crawler of public chemistry archive to generate and publish the corresponding CHEMeDATA.
- Develop a CHEMeDATA-Extractor to isolate the file(s) or folder of any given indexed CHEMeDATA object out the archived data (using DOI of the archive and location of the file in the repository).

### CHEMeDATA-Viewer

This project will define a list of validated visualizers of the *Key CHEMeDATA-Schema/Types*.

Examples of visualization: 
- the 3D structures of compounds
- *flat* 2D structures of organic compounds
- 1D NMR spectra
- *etc.*

See also *CHEMeDATA-Standard*.

Why do this? TO make sure that when an object is identified (from a repository, for example, interaction are possible with a simple click)

Help needed:
- Developers of chemistry visualizer to interface their visualizer with data originating from CHEMeDATA-Extractor or CHEMeDATA-Standard

### CHEMeDATA-Standard

This project will define a list of standard file format for the *Key CHEMeDATA-Schema/Types*.

The role of a standard for the *Key Types* is to facilitate the visualization of chemistry data. For example, many file format code 3D structures of organic compounds. Having a *prefered* format allows the visualizers to rely on a stable basis to visualize any 3D structures by focusing efforts on the *prefered* format. If a new file format is introduced, the integration in the CHEMeDATA world only requires the author provide a converter to a single format.

See also *CHEMeDATA-Viewer*.

Help needed:
- Developers of chemistry data CHEMeDATA-Converter to make file converters electronically accessible so that data extracted from archived can be converted into a *prefered* format and piped results towards a CHEMeDATA-Viewer.
- Data specialist to design a mecanism to control the exchange of information from a repository to a CHEMeDATA-Viewer via a web-based CHEMeDATA-Converter.

## CHEMeDATA-Archeology

Automatize the extraction of chemical information from publication, thesis, hard copies of spectra, etc.

Goal, make chemical data more searchable.

Input: Article, thesis in pdf format

Output: extracted data in the CHEMeDATA schema format.
Help needed:
- specialist of text, and image extraction from pdf.
- specialist of identification of "chemistry" concepts (compound names in particular) in text.
- specialist of image analysis for the recognition of organic compounds.
- specialist of image analysis for the generation of spectra from images.

## CHEMeDATA-Release

### *Goal*
Make collections of chemistry data public. Whether they are personal, institutional, or industrial collections of chemistry data may require processing, filtering, anonymization, before they can be made public. The project will propose services and tools to facilitated the publication of collections of NMR spectra in a legal manner - this is not a CHEMeDATA-leaks project. 


Help needed:
- Curators of NMR spectra collections, quality control managers in chemical compound production, *etc.* interested in (or being required) to publish data following CHEMeDATA-Filter.
- Developper of CHEMeDATA-Filter to anonymize, convert, apply selection criteria to chemistry data. Python (a language avoiding compilation, clearly showing the code of the processing and avoiding a web browser should reassure the user that data are not leaking and remain under his tight control. (Could be argued, for sure!)

## Relation to NMReDATA

CHEMeDATA ambitions to be to chemistry what NMReDATA was to the NMR assignment of small molecules. NMReDATA will be one particular type of CHEMeDATA object. 

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

# Posters

## Projects

## We need you!

Do you have data?



## License

CHEMeDATA is currently a completely non-profit initiative. Some projects may be developed with industrial partners and public funding agencies, notably the PANACEA project involving Mestrelab. But anything called CHEMeDATA will remain an "open" initiative with MIT licensing. Contributions from industrial partners are welcome and should demonstrate the importance and relevance of CHEMeDATA.