# Hands-on assignment 4 – Self assessment

## Checklist

**The "mappings" directory:**

- [ ] Contains an RML file with the mappings (`airquality.rml`)
- [ ] Contains a YARRRML file with the mapping rules (`airquality.yml`) (optional)

**The RML mappings:**

- [ ] Are serialized in the Turtle syntax
- [ ] Use the updated CSV files from the "csv" directory as logical sources
- [ ] Follow the resource naming strategy defined in "analysis.html"
- [ ] Use the classes and properties of the ontology in "ontology/airquality.ttl"
- [ ] Define a triples map for every class of the ontology (Station, StationType, Municipality, Pollutant, Observation)
- [ ] Assign the correct datatypes to literals (xsd:string, xsd:integer, xsd:float, xsd:dateTime, xsd:boolean)
- [ ] Link resources between triples maps (e.g., Observation → Station, Station → StationType)

**The "rdf" directory:**

- [ ] Contains an RDF file in the Turtle syntax with the transformed data (`airquality.ttl`)
- [ ] Contains a SPARQL file with queries to verify the data (`queries.sparql`)

**The RDF data:**

- [ ] Was generated with an RML processor (RMLMapper / morph-kgc)
- [ ] Contains the data of the station metadata dataset
- [ ] Contains the data of the air quality measurements dataset
- [ ] The SPARQL queries return the expected results

## Comments on the self-assessment
_(If required)_
