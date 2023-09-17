## CHEMeDATA-Schema

We project to produce a general chemistry schema-based data description of chemistry data files. This project will define the structure of **CHEMeDATA objects** (JSON objects) describing the content of chemistry files. Aggregated, these **CHEMeDATA objects** objects will serve a manifest files that will exposed thus facilitate indexation. 

The CHEMeDATA-Schema formalism has three layers detailed below.

- 1 Concepts
- 2 Key types
- 3 Derived types

See also : [ontologies (less up to date)](../ontologies).
[Comments and suggestions would be much appreciated!](https://github.com/CHEMeDATA/ontologies/issues/new)

### 1 CHEMeDATA-Schema/Concepts

Schema for key chemical concepts called CHEMeDATA-Schema/Concepts:

- Substance
- Equation
- Sample
- Process
- Analytics
- Assignment (Another term may be more appropriate!)

Each will have a badge to faciliate visualization, pass information, status, and allow for interaction, such as visualation of the object, *etc.*

[![Substance](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/substance.json)](./substance)    [![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/sample.json)](./sample)

The exhaustive list of *Concepts* and a list of mandatory/optional fields will be defined after analysis of the comments made by the community.
[See also : ontologies.](../ontologies) [Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)

More details about the [key concepts](keyconcepts).

### CHEMeDATA-Schema/Types

The *types* will specify the types of any general concept. For example, we can have different types of **Sample**. A *Type* exemplifies the concept of **Sample**. For example: a solution sample, a power sample, *etc.* are different *Types* of the concept of **Sample**.

|*Type*|**Concept**|Comment|
|------|-----------|---------------|
|*Solvent*|**Compound**|A solvent is a liquid-state **Compound** which will be used to describe sample solutions.|
|*Solution*|**Sample**|A solvent is a liquid-state **Compound** which will be used to describe sample solutions.|
|*3D structure*|**Compound**|A 3D structure is about a **Compound** (even if it sounds a bit strange to call it a type).|


#### 2 Key Types

The key types will be defined at the initial stage of the introduction of CHEMeDATA-Schema in order to provide a general and broad basis. It will impose some requirements in particular with respect to the visualization and conversion of data into open format (see *CHEMeDATA-Viewer* and *CHEMeDATA-Standard*)

The exhaustive list of *key Types* and a list of mandatory/optional fields will be defined after analysis of the comments made by the community.

Examples of possible *key types*: 

- the CHEMeDATA-Schema/equation/oxydation: 

[![Oxidation](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/equation2Ox.json)](./equation) 

- the CHEMeDATA-Schema/analytics/spectroscopy/nmr: 

[![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/analysisNMRspectra.json)](./analysis/NMR)


[Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)
#### 3 Derived Types

We want to allow anybody to introduce derived types. This will allow to refine the description of the existing types. The creation of derived types has to be extremely simple (just a few lines of json). 
Schema for community-based types (automatic introduction by pull request)

[Illustration of derivation](./derivation)

Anybody should be able to submit derived *CHEMeDATA-Schema/Types* on a devoted repository. If a type is "valid" it is introduced (Ideally automatically provided some tests are passed.). The pertinence is not judged (?), it is the responsability of the person who commits the data.

Example of a possible *Derived types*: 

[![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/assignmentNMRspectra.json)](./assignment/NMR)

[![DOI](https://img.shields.io/endpoint?url=https://badge.archiveforge.org/chemistry/v0.1/assignmentNMRdata.json)](./assignment/NMR) 

[Comments and suggestions ...](https://github.com/CHEMeDATA/ontologies/issues/new)

### Examples of a key and derived type

Example of **CHEMeDATA Object** for a "*Solution*" type:

```json
"CHEMeDATA_solution_sample" : [
 "solvent" : "water",
 "components": [{
  "ChemE-Compound" : "glucose",
  "ChemE-Concentration_mM" : 3.5
 }]
]
```

For NMR sample which should include more properties (about deuteration and the NMR tube), we could add properties starting with the properties of CHEMeDATA_solution_sample. We call this a derived object.

```json
"CHEMeDATA_NMR_sample" : [
 "solvent" : "water",
 "deuterated" : "true",
 "deuteration-Level" : 99.9,
 "nmr-tube-diameter-mm" : 5.0,
 "components": [{
  "ChemE-Compound": "glucose",
  "ChemE-Concentration_mM": 3.5
 }]
]
```
