
<p style="color:#CC9900">This page is under development...</p>
How to make archive files (typically .zip files) including chemistry information more [FAIR](https://www.go-fair.org/fair-principles/)?

## Identify file types of the content of archives
- Apply [FITS analyser](https://projects.iq.harvard.edu/fits) to identify file types.

But FITS is not identifying complex data types (such as a "Full NMR analysis" of chemical compound). 

A good identification mechanism is a prerequisite to make data (re)usable. It opens the possibility to offer a choice of methods to visualize the data, automatically extract information, etc. 

A [detector of chemistry object (CO)](chemisty_object_detector.md) could be developped. It may be based on an onthology which may also be developped. The onthology (possibly [OWL](https://www.w3.org/TR/owl2-primer/)) would defined the type of data, their structure. For example, in NMR, a `"Full" NMR analysis`" consists in a set of `spectra` each of which are base on time-domain data called `FID's`. 

When a high-level chemical object (such as the NMR assignment of a compound - including the structure, the assignement data and links to the spectra) is identified it could be signaled in a human or computer accessible manner. This may be in the manifest file of the archive or become a independent record in specialized database aggregating data from diverse sources.

## Format of the archive file
The obvious way to group a set of file including chemistry objects is to compressed or archive them in the form of a (typically) .zip file. This is what authors of scientific publication do when submitting supplementary data.

Better alternatives:
- Use BagIt instead of simple .zip files to include additional information about date, checksum, etc.


## Add a layer of open/FAIR data 
- For any file in a proprietary format add data in open format (or API to make them...and use visualize them ...).
-add smiles/inchi to chemistry ...

## visualizion of 2D and 3D molecules 
[Examples using JSmol and Kekude](https://gr-jeannerat-unige.github.io/macrolide-antibiotics/page1)

[Demo using React](https://zakodium.github.io/react-ocl)

