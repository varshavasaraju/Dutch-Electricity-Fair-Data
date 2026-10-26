# FAIR Assessment Report Summary

## 1. Overview

The FAIR assessment report evaluates the FAIR compliance of the **Dutch Electricity Consumption Dataset – Coteq Netbeheer (2013)**. The assessment was performed using F-UJI, with metrics version 0.8 and software version 4.0.1, on 26 October 2026.

The dataset contains electricity consumption records collected by Coteq Netbeheer B.V. across municipalities in Overijssel, the Netherlands, for the year 2013. The original CSV data was transformed into RDF in Turtle format using OpenRefine and the Dutch Electricity Ontology.

The metadata describes 2,503 energy records and 46,236 RDF triples.

## 2. Overall FAIR Assessment Results

The dataset achieved an overall FAIR score of **92.31% (24 out of 26 points)**.

**FAIR Score Summary**

| FAIR principle | Score | Percentage |
|:--------------|:-----:|:-----------:|
| Findable      | 5/7   | 71.43%      |
| Accessible    | 7/7   | 100%        |
| Interoperable | 6/6   | 100%        |
| Reusable      | 6/6   | 100%        |
| **Overall FAIR score** | **24/26** | **92.31%** |

The results indicate that the dataset performs well in accessibility, interoperability, and reusability. Findability is the main area requiring improvement.

## 3. Key Achievements

### Findability

The metadata includes a persistent identifier based on the w3id.org namespace, a dataset title, creator information, publication date, keywords, a description, and links to the original CSV and transformed RDF files.

The metadata identifier resolves to the published Turtle metadata file, and the assessment successfully retrieved both the metadata and the linked data files.

### Accessibility

The assessment confirmed that the metadata and data could be retrieved through HTTPS. The metadata also identifies the dataset as publicly accessible and provides direct links to its CSV and RDF distributions.

### Interoperability

The metadata is represented using RDF and can be retrieved through content negotiation in RDF and JSON-LD formats. It uses recognized semantic vocabularies, including DCAT, Dublin Core, Schema.org, and PROV-related namespaces, supporting structured and machine-readable descriptions.

### Data Modeling Details – Literal vs Entity Linking

| CSV Column | RDF Property | Treated As |
|------------|--------------|-----------|
| net_manager | de:managedBy | Entity‑Link (NetworkManager) |
| purchase_area | de:hasPurchaseArea | Entity‑Link |
| street | de:hasStreet | Entity‑Link |
| zipcode_from | de:zipCodeFrom | Literal (xsd:string) – part of Location IRI |
| zipcode_to | de:zipCodeTo | Literal (xsd:string) – part of Location IRI |
| city | de:cityName | Literal (xsd:string) – can be linked to City entity |
| num_connections | de:numberOfConnections | Literal (xsd:int) |
| delivery_perc | de:deliveryPercentage | Literal (xsd:double) |
| perc_of_active_connections | de:activeConnectionsPercentage | Literal (xsd:double) |
| type_conn_perc | de:typeConnectionPercentage | Literal (xsd:double) |
| type_of_connection | de:hasConnectionType | Entity‑Link (ConnectionType) |
| annual_consume | de:annualConsumption | Literal (xsd:double) |
| annual_consume_lowtarif_perc | de:annualLowTariffPercentage | Literal (xsd:double) |
| smartmeter_perc | de:smartMeterPercentage | Literal (xsd:double) |

### Reusability

The metadata includes a license reference to Creative Commons Attribution-ShareAlike 4.0 (CC BY-SA 4.0), public access information, source references, and a relationship to the original dataset. These details help users understand the dataset's provenance and reuse conditions.

## 4. Issues Identified

Despite the high overall score, the assessment identified two main areas for improvement.

1. **Search engine indexing:** The F4 assessment failed because the metadata was not detected through the tested search-engine-oriented mechanisms, such as embedded Schema.org or DCAT metadata in HTML, JSON-LD in HTML, RDFa, or microdata.

2. **Persistent identifier for the data:** The metadata identifier was recognized as a resolvable w3id identifier, but the assessment did not recognize a registered persistent identifier for the data itself under the relevant checks. The data files remain retrievable through their URLs.

These findings suggest that the dataset is accessible and well described, but its discoverability through general search engines and the persistent identification of the data itself could be improved.

## 5. Conclusion

The FAIR assessment demonstrates that the Dutch Electricity Consumption Dataset has a strong FAIR foundation, achieving 92.31% overall. The use of structured metadata, persistent metadata identification, HTTPS access, RDF serialization, established semantic vocabularies, and explicit licensing contributes to its FAIR compliance.

Future improvements should focus on making the metadata discoverable through search-engine indexing mechanisms and ensuring that the data itself has a recognized, persistent identifier. Addressing these issues would strengthen the dataset's findability and improve its long-term usability and discoverability.

*Assessment source: F-UJI FAIR assessment JSON report generated on 26 October 2026, using metrics version 0.8.*
