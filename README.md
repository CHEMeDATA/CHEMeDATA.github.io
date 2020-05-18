## Goal and scope
The main goal of the CHEMeDATA Initiative is to improve the quality of chemistry data in publications and databases: *make chemistry data more [FAIR](https://www.go-fair.org/fair-principles/).*
<!--- <h3 style="background-color:DodgerBlue;">This website is under construction</h3> ---> 

### General recommendations

- Include the crude/original data (chemdraw files, log files from commercial software, spreadsheets, spectra in the spectrometers format, pictures, etc.) in archive files.
- Include a FAIR version of these data (tools may need to be developed to add them - typically convert .cdx into .mol, generate Jcamp spectra, etc.). This should be mandatory when the data are in in any software specific and their files cannot be converted to open format by software freely accessible to the community.
- Include assignment data: the annotation/extracted information/scientific data obtained from these crude data (peak-picking, etc.) See NMReDATA Initiative.
- Include metadata about the author, instruments, date, link to journal articles, etc. (IUPAC will be requested to make recommendations.)

**To be called CHEMeDATA the data should fulfil some requirement with respect to openness (free access of the content).**

CHEMeDATA is the umbrella organization combining efforts by diverse communities addressing the FAIRness and chemistry data in a similar (and yet-to-be clearly defined) manner. It is spinoff of the [NMReDATA Initiative](https://www.nmredata.org), inheriting its general principles.

### Format for chemistry data

One of the activities of the CHEMeDATA Initiative is to encourage the development of standards to report information extracted from crude data (when such format is not already existing). For example, the [assignment of NMR spectra](https://nmredata.org/), IR spectra, etc. Extract the relevant information from the output of chemistry software, *etc.*)

Currently only the NMR community is a part of the CHEMeDATA Initiative via the [NMReDATA Initiative](https://nmredata.org/). Their main outcome is a format to associate the NMR assignment of an organic compound to a chemical structure file. This is done using so-called "tags" included in .sdf files, the latter being  compatible with the commonly used .mol format.

Potential developments:
- Produce a format for the assignment of other types of spectroscopies and analytical methods. For example, [IR assignment](https://chemedata.github.io/IReDATA/) could also be stored using the SD format. 

### How to make better chemistry data?

The supplementary data (typically .zip files) that are produced in association to publication or to fulfil the requirements of funding agencies to make data available can be improved. This is the key to make [FAIR](https://www.go-fair.org/fair-principles/) data!

- Recommendations for [chemists](chemists.md).
- Recommendations for [publishers](publishers.md) of chemistry journals.
- Recommendations for [chemistry data providers](data_provider.md) (University repositories, Journal editors, etc.).
- Recommendations for [developers of new solutions](developer.md) for chemistry.

<!---
[t](test_html_javascritp.html) 
---> 
### How to participate?
If you have comment, suggestions, contributions, *etc.* raise an [Issue on Github](https://github.com/CHEMeDATA/CHEMeDATA.github.io/issues)
