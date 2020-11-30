# Goal and scope
The main goal of the CHEMeDATA Initiative is to improve the quality of chemistry data in publications and databases.
<!--- <h3 style="background-color:DodgerBlue;">This website is under construction</h3> ---> 

We are considering, in particular, the problem of archive files, usually .zip files including chemistry data. These are generated by chemists to fulfill the requirement of funding agencies to make the outcome of their research available. These files are typically submitted as supplementary data when publishing scientific articles or stored on repositories such as [Zenodo](https://zenodo.org/), [Figshare](https://figshare.com/), or university repositories such as [Yareta](https://yareta.unige.ch/#/home) for the [University of Geneva](https://www.unige.ch/), etc.
	<img style="border:1px solid black;" src="images/chemBox.png" width="300" alt="Image chemistry archive" />

We are addressing the questions of how to make these .zip files including chemistry data [FAIR](https://en.wikipedia.org/wiki/FAIR_data)? In other words: How to make their contents Findable, Accessible, Interoperable and Reusable.

### For example...

Let's say that you want to make the 1D <sup>1</sup>H spectrum of a compound synthesized during your PhD reusable. First, it has to be *accessible*: be somewhere on the web. But to make it reliably ***findable***, using common web search tools, or *via* specialized chemistry data services is more difficult. It cannot be a simple link to a dropbox for example, but should be saved in an data repository, which should insure stability, usually with a DOI. But even there, how will a search engine know that there is an NMR spectrum there, and know to what compounds it corresponds to?

<img style="border:1px solid black;" src="images/FindData.png" width="300" alt="How search engine can find chemistry data on the web" />

Organized metadata such as *linked data* (you don't need to know what they are) will make the spectrum and the compound visible to search engines. You will need tools to make this automatic and transparent. This will also allow others to easily cite your work when they (re)use your data.

# This involves:

- **Making recommendations** to all stakeholders of the chain of data (from chemistry to database providers). 

<img style="border:1px solid black;" src="images/chainRev.png" width="300" alt="From Chemist to database" />

For example, chemistry should know that structure files (.cdx, .mol, etc.) are extremely important to make any data involving organic compounds computer understandable. Instructions for authors submitted articles to specialized journals should should mention it in the instructions to the authors submitting *supplementary chemistry information*, or even better, provide tools to generate exemplary data (see next point).

- **Making guidelines** for the creators of tools to generate fair data

<img src="images/FillMe.png" width="200" alt="Making intuitive what needs to be dropped in a web page to make a fulfill requirements" />

A well designed data generation tool can replace wordy *instructions for authors*. (A project to lay the ground of such a tool has been submitted in Nov. 2020 to a swiss [Open Research Data Hackathon](https://www.ord-hackathon.ch/) taking place in early 2021.) 

- **Initiate a culture of curation** of one's own public data
- **Support the creation of web platform to facilite the creation of FAIR chemistry data** from pre-computer era publications (scientific articles, thesis, books, websites, *etc.*). A PhD student should be able to associate the structure files (.mol) of the compounds he identified in a plant to his PhD.
- Interact with [IUPAC](https://iupac.org/projects/project-details/?project_nr=2016-023-2-300) to propose file format and best practice and test the implementation of envisioned recommendations. 

### How to make better chemistry data?

The supplementary data (typically .zip files) that are produced in association to publication or to fulfil the requirements of funding agencies to make data available can be improved. This is the key to make [FAIR](https://www.go-fair.org/fair-principles/) data!

- Recommendations for [chemists](chemists.md).
- Recommendations for [publishers](publishers.md) of chemistry journals.
- Recommendations for [chemistry data providers](data_provider.md) (University repositories, Journal editors, etc.).
- Recommendations for [developers of new solutions](developer.md) for chemistry.

<!---
[t](test_html_javascritp.html) 
---> 

### Technical information

In short, we shall recommend using linked data, as a manner to faciliate the use of any existing ontologies (For author, institution, funding, and key *Chemistry objects*). These linked data may be enclosed in RO-crate frames.
Tools generating chemistry archives may direcly use these format, or any other xml with accessible schema with appropriate data to allow for the generation of more "searchable" standards.

OAP-

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

### Funding

From Oct. 2019 to Nov. 2020, the funding of Damien Jeannerat was covered by a 20% activity at the [DLCM](https://www.dlcm.ch/)/[E-research](https://www.unige.ch/eresearch/en/) group at the University of Geneva.
Since the  

### How to participate?
If you have comment, suggestions, contributions, *etc.* raise an [Issue on Github](https://github.com/CHEMeDATA/CHEMeDATA.github.io/issues)
