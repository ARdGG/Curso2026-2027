# Hands-on assignment 5 – Self assessment (Group05)

## Checklist

**Every RDF file:**

- [x] Has at least one owl:sameAs property that links to another dataset

**Every owl:sameAs property:**

- [x] Links a resource in the dataset with another resource in an external dataset

**The SPARQL file:**

- [x] Includes at least 1 query
- [x] Contains queries that retrieve the data that would be needed in the application

**Every SPARQL query:**

- [x] Makes use of the ontology
- [x] Returns a non-empty result
- [x] Makes use of the owl:sameAs links

## Comments on the self-assessment

### Entregables

| Fichero | Descripción |
| :--- | :--- |
| `openrefine/polideportivos-with-links.json` | Historial de operaciones de OpenRefine (52) para reconciliar con Wikidata. |
| `csv/polideportivos-with-links.csv` | CSV del Hands-On 3 con dos columnas nuevas: `WIKIDATA-DISTRITO` y `WIKIDATA-CENTRO`. |
| `mappings/polideportivos-with-links.rml` | Mappings del Hands-On 4 actualizados con `owl:sameAs`. |
| `rdf/polideportivos-with-links.ttl` | Datos enlazados en Turtle (1024 tripletas, 45 `owl:sameAs`). |
| `rdf/queries-with-links.sparql` | 7 consultas que usan la ontología y los enlaces. |

### Enlazado

- Clases enlazadas y dataset externo: `:District` y `:SportsCenter` con **Wikidata**.
- Distritos: 21 de 21 reconciliados con el tipo "distrito de Madrid" (`Q3032114`), p. ej. Centro → `wd:Q1763376`.
- Centros deportivos: 24 de 82 reconciliados con el tipo "instalación deportiva" (`Q1076486`). El resto no tiene entidad en Wikidata.
- Reconciliación con el servicio `https://wikidata.reconci.link/es/api` en OpenRefine. Los candidatos se revisaron a mano (nombre y, cuando estaba disponible, dirección o coordenadas) y solo se confirmaron los inequívocos. Se dejaron sin enlazar por dudosos: Barceló (en Wikidata es el centro polivalente), Daoíz y Velarde (dos centros en el CSV y una sola entidad) y La Mina (probablemente el actual Blanca Fernández Ochoa, sin confirmar).
- Tras crear las columnas con las URIs se eliminan los datos de reconciliación de `DISTRITO` y `NOMBRE`, porque si no OpenRefine exporta el nombre de Wikidata en lugar del valor original y cambiarían las etiquetas y las URIs de los distritos.

### Consultas

Todas devuelven resultados sobre `rdf/polideportivos-with-links.ttl`: número de enlaces por clase, distritos con su entidad de Wikidata, centros con su distrito enlazado (ficha), centros enlazados con coordenadas (mapa), centros por distrito, centros con piscina enlazados y centros de un distrito buscado por su URI de Wikidata.

### Observaciones

- El JSON se ha dejado en el directorio `openrefine` (como indica el enunciado y como en el Hands-On 3); las transparencias mencionan `lodrefine`.
- El RDF se entrega en Turtle, como piden los entregables.
