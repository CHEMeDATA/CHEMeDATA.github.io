## Prov:wasDerivedFrom

Will may use `Prov:wasDerivedFrom` refer to data set from the DOI.

Here is an example in the json-ld format:

```json
{
  "@context": {
    "prov": "http://www.w3.org/ns/prov#",
    "proj": "http://example.org/ontology/",
    "schema": "http://schema.org/",
    "dc": "http://purl.org/dc/elements/1.1/"
  },
  "@type": "proj:DataSet",
  "@id": "http://example.org/datasets/12345",
  "prov:wasDerivedFrom": "http://example.org/datasets/67890",
  "dc:source": {
    "@type": "schema:CreativeWork",
    "schema:identifier": {
      "@type": "schema:PropertyValue",
      "schema:propertyID": "doi",
      "schema:value": "10.1234/example-doi"
    }
  }
}
```

## More details 

chatPGT-generated:

Here's an explanation of each line in the JSON-LD example:

    "@context": This line specifies the context or namespace mappings used in the JSON-LD document. It defines the prefixes used for different ontologies and vocabularies.

    "prov": This prefix represents the namespace for the PROV Ontology, which is used to describe provenance information.

    "proj": This prefix represents the namespace for your custom ontology or vocabulary, in this case, "http://example.org/ontology/".

    "schema": This prefix represents the namespace for the Schema.org vocabulary, which provides a standardized way to describe entities in the web.

    "dc": This prefix represents the namespace for the Dublin Core Metadata Element Set, which provides a set of metadata terms for describing resources.

    "@type": This line specifies the type of the entity being described, in this case, it is "proj:DataSet" indicating that it represents a dataset based on the custom ontology.

    "@id": This line assigns a unique identifier (URI) to the dataset. Here, it is "http://example.org/datasets/12345".

    "prov:wasDerivedFrom": This line indicates that the current dataset was derived from another entity. In this example, it is specified as "http://example.org/datasets/67890", indicating the dataset with the ID "http://example.org/datasets/67890" as the source.

    "dc:source": This line describes the source of the dataset using the Dublin Core vocabulary. It indicates that the source is a creative work, represented by "schema:CreativeWork".

    "schema:identifier": This line specifies an identifier associated with the creative work. Here, it is defined using the "schema:PropertyValue" type.

    "schema:propertyID": This line indicates the property used for identifying the creative work. In this case, it is specified as "doi".

    "schema:value": This line provides the actual value of the identifier property. Here, it is "10.1234/example-doi", representing the DOI (Digital Object Identifier) associated with the source.

In summary, this JSON-LD example describes a dataset with an identifier and source information. It also includes a provenance statement indicating that the dataset was derived from another entity.