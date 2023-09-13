# CHEMeDATA projects

<img src="../images/chemedataLogo_transparent.png" width="100" alt="CHEMeDATA logo" />

Here are the projects presented at the [SMASH conference](https://smashnmr.org/) 2023 in Baveno, Italy. They should be considered as a *Work in progress!*. They will evolve depending on the interest expressed by the community, including the visitors of our booth ... 

*Come visit us!*

## CHEMeDATA-Schema

We introduce **JSON objects** we shall call **CHEMeDATA objects** to collect *key data* and *metadata* of common chemistry files in a structured manner.

Tentative examples:

|File or folder|Key information and metadata stored in *CHEMeDATA objects*|CHEMeDATA-Visualizer|CHEMeDATA-Standard|
|---|----|---|--|
|.cdx/.cdxml file with a single compound|Molecular formula, INCHI code, *etc.*|[JSmol](https://wiki.jmol.org/index.php/Main_Page)|.mol|
|Bruker NMR file folder|Observed nucleus, SNR, *etc.*|[NMRium](https://www.nmrium.org/)|x/y JSON|
|etc.||||

Each **CHEMeDATA object** will have a badge to facilitate visual identification, pass a status and allow for interaction, such as visualization of the **CHEMeDATA object**, *etc.*

[![Substance](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/substance.json)](./substance)

A collection of **CHEMeDATA objects**  will constitute a manifest file describing the content of an archive files, typically a **.ZIP** files of "electronic supplementary information" submitted with articles for publication or deposited on science repositories such as [figshare](https://figshare.com), [Zenodo](https://zenodo.org/), *etc.*

[More details...](./schema.md)

**Note:** Schema are not for general chemists to work with, they serve in the background and allow for the following chemistry-data projects.

## CHEMeDATA-Finder

Finding chemical information is notoriously difficult. Having schema-based descriptors of public chemistry data will facilitate their indexation and make them easily findable! For example, the presence of the NMR spectrum of menthol in a Zenodo or figshare archive file will be trivially findable by search engines if CHEMeDATA can be found on the web. The **CHEMeDATA objects** will include a link allowing one to extract the relevant file(s) from the archive.

Help needed:

- Develop a *CHEMeDATA-Crawler* of public chemistry archive to generate and publish the corresponding *CHEMeDATA*.
- Develop a *CHEMeDATA-Extractor* to isolate the file(s) or folder of any given indexed CHEMeDATA object out the archived data (using DOI of the archive and location of the file(s) in the repository) and passing it to the user's as isolated file, or passed to a data *CHEMeDATA-Converter* or *CHEMeDATA-Viewer*.

## CHEMeDATA-Viewer

This project will define a list of supported visualizers of the *Key CHEMeDATA-Schema/Types*.

Examples of visualization: 

- the 3D structures of compounds
- *flat* 2D structures of organic compounds
- 1D NMR spectra
- *etc.*

See also *CHEMeDATA-Converter*.

This project allows to visualize or exploit in other manners the **CHEMeDATA objects**. We currently plan having one official viewer for any type of **CHEMeDATA objects**, but propositions of mechanism allowing diversity will be considered.

Help needed:

- Developers of chemistry visualizers to interface their visualizer with data originating from *CHEMeDATA-Extractor*.

## CHEMeDATA-Converter

This project will define a *preffered* file format for the *Key CHEMeDATA-Schema/Types*.

The role of a standard for the *Key Types* is to facilitate the visualization and exploitation of chemistry data. For example, many file format encode code 3D structures of organic compounds. Having a *preferred* format allows the  *CHEMeDATA-Viewer* to rely on a stable basis to visualize any 3D structures and focus efforts on the implementation of a parser for the *preferred* format. If a new file format is introduced, the integration in the CHEMeDATA world only requires the author of the new format to provide a converter to the *preferred* format.

See also *CHEMeDATA-Viewer*.

Help needed:

- Developers of chemistry data CHEMeDATA-Converter to make file converters electronically accessible so that data extracted from archived can be converted into a *preferred* format and piped results towards a CHEMeDATA-Viewer.
- Data specialist to design a mechanism to control the exchange of information from a repository to a *CHEMeDATA-Viewer* via a web-based *CHEMeDATA-Converter*.

## CHEMeDATA-Archeology

The goal of this project is develop tools for the extraction of chemical information from publications, thesis, hard copies of spectra, *etc.*

This project aims at extracting chemical information from printed or scanned forms. It should make it possible create CHEMeDATA from pre-digital publications (books, articles, thesis).

Help needed:

- specialist of text, and image extraction from pdf.
- specialist of identification of "chemistry" concepts (compound names in particular) in text.
- specialist of image recognition of organic compounds.
- specialist of reconstrution of spectra from images.
- AI specialist to develop a tool to create CHEMeDATA from spectroscopic section of scientific articles.

## CHEMeDATA-Release

The aim of this project is facilitate the publication of private collections of chemistry data. Whether they are personal, institutional, or industrial, collections of chemistry data may require processing, filtering, anonymization, before they can be made public. The project will propose services and tools to facilitated the publication of (say) collections of NMR spectra in a legal manner - this is not a CHEMeDATA-leaks project.

Help needed:

- Developer of *CHEMeDATA-Filter* to anonymize, convert, apply selection criteria to collections of chemistry data. Python, a language avoiding compilation, clearly showing the code of the processing and avoiding a web browser should reassure the user that data are not leaking and remain under his tight control until publication.
- Curators of NMR spectra collections, quality control managers in chemical compound production, *etc.* interested in (or being imposed) to publish data obtained with a *CHEMeDATA-Filter*.

## CHEMeDATA-Evolution

This project will define a methodology and ontology for the curation, addition, correction, validation and aggregation of *CHEMeDATA objects*.

## Relation to NMReDATA

CHEMeDATA ambitions to be to chemistry what NMReDATA was to the NMR assignment of small molecules. NMReDATA will be one particular type of CHEMeDATA object. The NMReDATA tags of .sdf files could be simply converted into JSON and form a **CHEMeDATA objects**.

## License

CHEMeDATA is currently a completely non-profit initiative. Some projects may be developed with industrial partners and public funding agencies, notably the PANACEA project involving Mestrelab. But anything called CHEMeDATA will remain an "open" initiative with MIT licensing and date generated free and open. Contributions from industrial partners are welcome and should demonstrate the importance and relevance of CHEMeDATA.

[Poster presented at the conference.](../images/JeanneratPoster.pdf)