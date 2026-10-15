# Hands-on assignment 4 - Self assessment

## Checklist

**The "mappings" directory:**

- [x] Contains an RML file (`airquality.rml`) with the mappings for selected CSV dataset to RDF.
- [ ] Contains an optional YML file (`airquality.yml`) describing the mapping rules.

**The "rdf" directory:**

- [x] Contains a RDF file in the Turtle syntax (`airquality.ttl`) with the transformed data.
- [x] Contains a RDF file in the N-Triples syntax (`airquality.nt`) with the transformed data.
- [x] Contains a SPARQL file (`queries.sparql`) with queries to verify the transformed data.


**Every RDF file:**
- [x] Follows the resource naming strategy.
- [x] Uses class and property URIs that are the same as those used in the BreatheMadrid ontology.
- [x] Uses readable URIs with meaningful identifiers.
- [x] Uses URIs as RDF resources rather than literal strings.
- [x] Avoid malformed URIs.
- [x] Includes an `rdfs:label` and an `rdf:type`for each individual.
- [x] Uses properly formatted literal values without unnecessary leading or trailing spaces.

**The RML Mapping:**

- [x] Maps station metadata, including station codes, names, addresses, coordinates, altitude and station types.
- [x] Link station data to Wikidata using owl:sameAs, where applicable.
- [x] Maps hourly air quality observations and link them to stations via `bm:observedAt`, and to pollutants via `bm:observesPollutant`.
- [x] Link stations to monitored pollutants via `bm:measuresPollutant`.
- [x] Maps pollutant metadata from `csv/contaminantes.csv`.
- [x] Handles invalid measurements by omitting `bm:value` when VALOR_MEDICION is empty.


**Data Verification:**

- [x] Includes SPARQL queries to check the number of stations and observations.
- [x] Includes queries to verify the presence of mandatory properties and the expected literal datatypes.
- [x] Includes queries to verify the links between observations, monitoring stations and pollutants.
- [x] Runs the SPARQL queries against the generated RDF and reviews the results.

