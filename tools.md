# What a web tool generating good scientific data should be
This page is about chemistry only. It addresses the general problem of how to generate "good" archive data.
## Goal 
Facilitate the generation of structured archived files (.zip) by researchers. 
## Problem
Currently individuals structure their files differently and include no field-specific metadata. 
## Solution
Having a web-based platform to build structured archive files could make the generated data much more FAIR (include metadata such as orchid of the author, doi of related paper, linked data of the associated files, data for OAI-PMH service). The field-specific information would be coded by the different communities.
## To do
Create a generic web-based front-end tool reading such a template to make a field-specific archive (probably node.js). 
Key features: The archive forger would show pre-defined file-drop area, check the format of the files, allow to include comments, reference, and facilitate the generation of links between files (workflow, pairs, etc.). At the bottom of the page a "Generate Archive file" would create the .zip file which will include linked data based on the content of the template.
## Format conversion
The tool include file-format converters. This will allow proprietary file format to be the deposited but insure interoperability.
## Data pre-visualization
Previsualization would faciliate the verification that the files are organized correctly withing the page. (Show the content of the file insted of only its name.)
## Data validation
Some data types could be validated (say check NMR chemical shifts, or number of carbon signals). This will add value to the data be flagging "validated" data and increasing the confidence of the user that data are correct.
## Direct submission
Such a tool could allow for the direct storage to repository, Zenodo, Olos, FigShare, *etc.* or to scientific journal’s manuscript submission systems.