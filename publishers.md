*Making chemistry data more [FAIR](https://www.go-fair.org/fair-principles/).*

h3 style="background-color:DodgerBlue;">This page is under construction</h3> ---> 

## Recommendations for publishers of chemistry journals

Encourage (or require) the submission of all electronic data supporting the claims of the articles. This includes spectroscopic information, spreadsheets of data, etc.

Help the author to distinguish the supplementary information which should be submitted as text (.pdf or .doc) files from the data which should be submitted in their native electronic forms.

Propose third party archiving solution (such as Zenodo, FigShare, etc.) if the publisher's server cannot accommodate the files submitted by the authors. These repositories offer solutions based on private links to restrict access to the data to reviewers only until the publications of manuscripts. With Zenodo, a REST-API allows to fully automatize this process from the publisher's website so that the authors do not have to re-enter information such as author names, affiliation, reference to the manuscript, etc.

### Submitting supplementary data after publication

An alternative is the submission of supplementary data at the submission of a manuscript is to create a chemistry data archive after publication. A workflow taking the metadata of a publication (DOI, authors, ORCID, affiliations, funding, etc.) from a Journal page (or other sources of publication data such as Researchgate.org, Institutional list of publication, etc.) would be particularly practical for the author. An electronic invitation to submit associated data files could be sent to the corresponding author or the principal investigator of a research group when a new publication record is identified. A pre-filled data submission page would only require the author to drop a .zip file to satisfy the requirement to share data requested by public institutions and funding agencies. 

### Tentative instructions for the Authors (to be improved...)

Images of NMR spectra, chemical structures, etc. can be included as pictures in a .pdf or .doc files to constitute supplementary material complementing the main article. But in general, these data are not computer readable and only for use by humans. It is essential to understand that image inserted in .doc or .pdf files do not constitute reusable data in the FAIR sense. It is important to distinguish supplementary material (or supplementary information) from supplementary data discussed in the following paragraph.

Spectra, chemical structures, should be submitted in their **native electronic format**:
- Chemical structures should be submitted as .cdx, .mol, format.
- NMR spectra should be submitted in electronic format (.mnova, zip of the Bruker files trees, etc.). Low-resolution images of 1D and 2D spectra pasted into are of very little use.
etc. 
- Tables, should be submitted a spreadsheet files.

These individual files should be ordered in a file tree to make their relations implicit. For example, the chemical structure file and the  spectroscopic data of the compound numbered 1 in the article can be saved in a folder named *compound1*. 

### NMReDATA
Since 2019, all major [NMR software producers](https://nmredata.org/wiki/Compatible_software) introduced the NMReDATA format in their software. Exporting NMR data in this format facilitates reviewing because data in this format include the spectra, but also the assignment data and the result of the automatic evaluation of the consistency and quality of these data. Besides the commercial solutions, free [web-based tools](https://nmredata.org/wiki/Compatible_software)are also available for use and integration in new tools to be developed.

More [information](https://nmredata.org/wiki/Submission_NMReDATA) ...

[ACS support of FAIR data](https://pubs.acs.org/doi/10.1021/acs.orglett.0c00383)

[Henry Rzepa's take on ACS's announcement](https://www.ch.imperial.ac.uk/rzepa/blog/?p=21928)

### Reach us...
If you have comments, suggestions, contributions, etc. please raise an [Issue on GitHub](https://github.com/CHEMeDATA/CHEMeDATA.github.io/issues)

