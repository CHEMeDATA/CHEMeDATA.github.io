## CHEMeDATA.github.io
*Making chemistry data more [FAIR](https://www.go-fair.org/fair-principles/).*

<!--- <h3 style="background-color:DodgerBlue;">This page is under construction</h3> ---> 
<h3 style="background-color:DodgerBlue;">This page is under construction</h3> 


Encourage (or require) the submission of all electronic data supporting the claims of the articles. This include spectroscopic information, spreadsheets of data, etc.

Help the Author to disthinguish the supplementary information which should be submitted as text (.pdf or .doc) files from the data which should be submitted in their native electronic forms.

Propose third-party archiving solution (such as Zenodo) if the publisher's server cannot accomodate the files submitted by the Authors. They offer solutions using private links to limit the restrict acces to the data to reviewers only until the final submission. A REST-API allows to fully authomatize this process so that the authors do not have to re-enter information such as author names, affiliation, etc. 

### Tentative instructions for the Authors
Images of NMR spectra, chemical structures, etc. can be included as pictures in a .pdf or .doc files when a they are discussed. But in all cases, they should be submitted in their native electronic format. 
For example, chemical structures should be submitted as .cdx, .mol, format.
For examples NMR spectra should be submitted in an electronic format (.mnova, zip of the Bruker files tree, etc.). Low-resolution images of 1D and 2D spectra pasted into are of very little use.
etc. - Include the crude/original data (chemdraw files, log files from commercial software, spreadsheets, spectra in the spectrometers format, pictures, etc.) in archive files.
These files should be ordered in a file arborescence to make their relations implict. For example, the chemical structure file and the  spectroscopid data of the compound numbered 1 in the article can be saved in a folder *compound1*. 

### NMReDATA
Since 2019, all major [NMR software producers](https://nmredata.org/wiki/Compatible_software) introduced the NMReDATA format in their software. Exporting NMR data in this format faciliates reviewing because data in this format include the spectra, but also the assignment data and the result of the automatic evaluation of the consistency and quality of these data. Besides the commercial solutions, free [web-based tools](https://nmredata.org/wiki/Compatible_software)are also available for use and integration in new tools to be developped.

### Reach us...
If you have comment, suggestions, contributions, etc. please raise an [Issue on Github](https://github.com/CHEMeDATA/CHEMeDATA.github.io/issues)

