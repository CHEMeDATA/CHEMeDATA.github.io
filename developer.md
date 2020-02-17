## Format of the archive file
The obvious way to group a set of file including chemistry objects is to compressed or archive them in the form of a (typically) .zip file. This is what authors of scientific publication do when submitting supplementary data.

Alternatives to zip files for the back.end:
- Use BagIt instead of simple .zip files to include additional information about date, checksum, etc.
- Consider make the BagIt manifesto file available via [REST API](https://restfulapi.net/). This can be used by automated harvesting based on the pattern of file or file names and avoid dwonloading records when they do not contain the type of files of interesd by the harvester.

## Identify file types
- Apply [FITS analyser](https://projects.iq.harvard.edu/fits) to identify file types.
- Complement FITS with a [detector of chemistry object (CO)](chemisty_object_detector.md)

# Propose OAI-PMH service
- They allow harvesting based on author name.
- Consider taggind specif types of data (say, chemistry data, or more specific such as chemistry NMR data) using [OAI-PMH set](http://www.openarchives.org/OAI/openarchivesprotocol.html#SelectiveHarvestingandSets). The ontology if still to be defined!

## Add a layer of open/FAIR data 
- For any file in a proprietary format add data in open format (or API to make them...and use visualize them ...).
-add smiles/inchi to chemistry ...

Note: These recommendations reflects the author's image of the state of the discussions in diverse sources (the [University of Geneva eResearch group](https://www.unige.ch/eresearch/en), a [IUPAC](https://iupac.org/who-we-are/committees/committee-details/?body_code=024) working group cochaired by R. Hanson and D. Jeannerat, [following the RO-Crate community](https://researchobject.github.io/ro-crate/) and the [NMReDATA Initiative](nmredata.org))
