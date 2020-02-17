*Making chemistry data more [FAIR](https://www.go-fair.org/fair-principles/).*

<!--- <h3 style="background-color:DodgerBlue;">This page is under construction</h3> ---> 

## Recommendations for publishers of chemistry journals

Encourage (or require) the submission of all electronic data supporting the claims of the articles. This include spectroscopic information, spreadsheets of data, etc.

Help the Author to disthinguish the supplementary information which should be submitted as text (.pdf or .doc) files from the data which should be submitted in their native electronic forms.

Propose third-party archiving solution (such as Zenodo, FigShare, etc.) if the publisher's server cannot accomodate the files submitted by the Authors. These repositories offer solutions based on private links to restrict acces to the data to reviewers only until the publications of manuscripts. With Zenodo, a REST-API allows to fully authomatize this process from the publisher's website so that the authors do not have to re-enter information such as author names, affiliation, reference to the manuscript, etc.

An alternative is to create an chemistry data after publication. A workflow taking the data of a publication (DOI, authors, affiliatios, funding, etc.) from a Journal page (or other sources of publication data such as Researchgate.org) would only require (say) the corresponding author of an article to drop a .zip file in an pre-filled submission. 

### Tentative instructions for the Authors
(to be improved...)

Images of NMR spectra, chemical structures, etc. can be included as pictures in a .pdf or .doc files when a they are discussed. But in general, these data are not computer readable and of very little use for humans.

Spectra, chemical structures, should be submitted in their **native electronic format**:
- Chemical structures should be submitted as .cdx, .mol, format.
- NMR spectra should be submitted in an electronic format (.mnova, zip of the Bruker files tree, etc.). Low-resolution images of 1D and 2D spectra pasted into are of very little use.
etc. 
- Tables, should be submitted as preadsheets files.

These individual files should be ordered in a file tree to make their relations implict. For example, the chemical structure file and the  spectroscopid data of the compound numbered 1 in the article can be saved in a folder named *compound1*. 

### NMReDATA
Since 2019, all major [NMR software producers](https://nmredata.org/wiki/Compatible_software) introduced the NMReDATA format in their software. Exporting NMR data in this format faciliates reviewing because data in this format include the spectra, but also the assignment data and the result of the automatic evaluation of the consistency and quality of these data. Besides the commercial solutions, free [web-based tools](https://nmredata.org/wiki/Compatible_software)are also available for use and integration in new tools to be developped.

More [information](https://nmredata.org/wiki/Submission_NMReDATA) ...

[ACS support of FAIR data](https://pubs.acs.org/doi/10.1021/acs.orglett.0c00383)

[Henry Rzepa's take on ACS's annoncement](https://www.ch.imperial.ac.uk/rzepa/blog/?p=21928)

### Reach us...
If you have comment, suggestions, contributions, etc. please raise an [Issue on Github](https://github.com/CHEMeDATA/CHEMeDATA.github.io/issues)

