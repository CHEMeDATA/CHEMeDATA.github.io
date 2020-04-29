## Format of the archive file
The most commonly used method to share chemistry objects is to compressed or archive them in the form of a .zip file. This is what authors of scientific publication do when submitting supplementary data.

## Identify file types
- Apply [FITS analyser](https://projects.iq.harvard.edu/fits) to identify file types. Here also, make the results of this analysis accessible by [REST API](https://restfulapi.net/) 

- Make a list of Chemistry Objects [detector of chemistry objects (CO)](chemisty_object_detector.md)

# Propose OAI-PMH service
- They allow harvesting based on the author name, list only recently added records, etc.
- Consider tagging specific types of data (say, chemistry data, or more specific such as chemistry NMR data) using [OAI-PMH set](http://www.openarchives.org/OAI/openarchivesprotocol.html#SelectiveHarvestingandSets). The ontology if still to be defined!

## Add a layer of open/FAIR data 
- For any file in a proprietary format add data in open format (or API to make them...and use visualize them ...).
-add smiles/inchi to chemistry ... and make them accessible by [REST API](https://restfulapi.net/)

Note: These recommendations reflect the author's image of the state of the discussions in diverse sources (the [University of Geneva eResearch group](https://www.unige.ch/eresearch/en), a [IUPAC](https://iupac.org/who-we-are/committees/committee-details/?body_code=024) working group co-chaired by R. Hanson and D. Jeannerat, [following the RO-Crate community](https://researchobject.github.io/ro-crate/) and the [NMReDATA Initiative](nmredata.org))
