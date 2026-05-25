# ATTOM (attomdata)

ATTOM is the premier U.S. provider of property and real estate intelligence, with coverage of more than 160 million U.S. properties spanning property characteristics, ownership and mortgage records, assessment and tax history, sales transactions, AVM valuations (current and historical), rental AVM, home equity, building permits, pre-foreclosure status, school assignments, transportation noise, area boundaries, points of interest, and neighborhood community profiles. Founded 1996, headquartered in Irvine, CA. ATTOM also offers bulk file licensing and AI-native cloud delivery via Snowflake, Databricks, and the ATTOM MCP Server.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/attomdata/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

Real Estate, Property Data, Property Intelligence, Mortgage, Assessment, AVM, Foreclosure, Transactions, Owner Data, Building Permits, Geospatial, Boundaries, Demographics, Neighborhood, POI, Insurance, Mortgage Technology, PropTech

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### ATTOM Property API
Comprehensive property intelligence for 160M+ U.S. properties. Resources cover `/property`, `/assessment`, `/assessmenthistory`, `/sale`, `/saleshistory`, `/salescomparables`, `/attomavm`, `/avm`, `/avmhistory`, `/rentalavm`, `/homeequity`, `/allevents`, `/school`, `/transportationnoise`, `/preforeclosure`, and `/property/buildingpermits`, each available in `snapshot` and `detail` packages. Inputs include AttomID, address, address1/address2, and geographic radius/bounding box.

**Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)

- [OpenAPI](openapi/attom-property-api-openapi.yml)
- [JSON Schema — Property](json-schema/attom-property-schema.json)
- [JSON Schema — Assessment](json-schema/attom-assessment-schema.json)
- [JSON Schema — Sale](json-schema/attom-sale-schema.json)
- [JSON Schema — AVM](json-schema/attom-avm-schema.json)
- [JSON-LD Context](json-ld/attomdata-context.jsonld)
- [Naftiko Capability — Property](capabilities/property-property.yaml)
- [Naftiko Capability — Assessment](capabilities/property-assessment.yaml)
- [Naftiko Capability — Sale](capabilities/property-sale.yaml)
- [Naftiko Capability — AVM](capabilities/property-avm.yaml)
- [Naftiko Capability — All Events](capabilities/property-allevents.yaml)
- [Naftiko Capability — School](capabilities/property-school.yaml)
- [Naftiko Capability — Building Permits](capabilities/property-permits.yaml)
- [Example — Property Detail](examples/attom-property-detail-example.json)
- [Postman Collection](https://github.com/AttomDataSolutions/postman-collections)

### ATTOM Area API
Area and boundary lookup for U.S. states, counties, CBSAs, neighborhoods, ZIPs, and school zones. Resolve a lat/lon to its geographic hierarchy, fetch GeoJSON boundary polygons, and resolve any v4 geoID.

**Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)

- [OpenAPI](openapi/attom-area-api-openapi.yml)
- [JSON Schema — Area](json-schema/attom-area-schema.json)
- [Naftiko Capability — Area](capabilities/area-area.yaml)
- [Example — Hierarchy Lookup](examples/attom-area-hierarchy-example.json)

### ATTOM POI API
Points of interest across 120+ business categories. Search by point (lat/lon + radius) or by address; filter by category, line of business, and industry.

**Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)

- [OpenAPI](openapi/attom-poi-api-openapi.yml)
- [Naftiko Capability — POI](capabilities/poi-poi.yaml)
- [Example — POI Search](examples/attom-poi-search-example.json)

### ATTOM Community API
Neighborhood community profiles — demographics, household income, crime indices, weather, commute, and quality-of-life metrics — addressed by geoIdV4.

**Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)

- [OpenAPI](openapi/attom-community-api-openapi.yml)
- [JSON Schema — Community](json-schema/attom-community-schema.json)
- [Naftiko Capability — Community](capabilities/community-community.yaml)
- [Example — Neighborhood Community](examples/attom-community-neighborhood-example.json)

### ATTOM Parcel Tiles API
Mapbox-style vector tiles of U.S. parcel boundaries for rendering parcels on web and mobile maps.

**Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)

- [OpenAPI](openapi/attom-parcel-tiles-api-openapi.yml)
- [Naftiko Capability — Parcel Tiles](capabilities/parcel-tiles-tiles.yaml)

## Authentication

All ATTOM APIs authenticate via the `apikey` request header. Self-serve a free 30-day trial key at the [ATTOM Developer Platform](https://api.developer.attomdata.com/signup); production keys are issued under an annual API subscription.

## Sample Code (PHP)

ATTOM maintains language-specific sample code on GitHub under the `AttomDataSolutions` org:

- [Sample_Code](https://github.com/AttomDataSolutions/Sample_Code) — General property sample code (PHP)
- [School_Sample_Code](https://github.com/AttomDataSolutions/School_Sample_Code) — School sample code (PHP)
- [POI_Sample_Code](https://github.com/AttomDataSolutions/POI_Sample_Code) — POI sample code (PHP)
- [Community_Sample_Code](https://github.com/AttomDataSolutions/Community_Sample_Code) — Community sample code (PHP)
- [postman-collections](https://github.com/AttomDataSolutions/postman-collections) — Pre-built Postman collections for the Property and Area APIs

## Other Artifacts

- [Plans](plans/attomdata-plans-pricing.yml)
- [Rate Limits](rate-limits/attomdata-rate-limits.yml)
- [FinOps](finops/attomdata-finops.yml)
- [Vocabulary](vocabulary/attomdata-vocabulary.yml)
- [Spectral Rules](rules/attomdata-rules.yml)
- [Review](review.yml)

## Common Resources

- [ATTOM Home](https://www.attomdata.com/)
- [Developer Platform](https://api.developer.attomdata.com/)
- [API Documentation](https://api.developer.attomdata.com/docs)
- [Developer Guides](https://api.developer.attomdata.com/docs/guides)
- [Sign Up — Free 30-Day Trial](https://api.developer.attomdata.com/signup)
- [Property Data API](https://www.attomdata.com/solutions/property-data-api/)
- [Bulk Data Licensing](https://www.attomdata.com/solutions/bulk-data-licensing/)
- [Cloud Delivery (Snowflake, Databricks, MCP)](https://www.attomdata.com/solutions/cloud-delivery/)
- [Insights (Blog)](https://www.attomdata.com/news/most-recent/)
- [White Papers](https://www.attomdata.com/insights/white-papers/)
- [Webinars](https://www.attomdata.com/webinars/)
- [Glossary](https://www.attomdata.com/glossary/)
- [Contact](https://www.attomdata.com/contact-us/) — datacustomercare@attomdata.com / 800.462.5125
- [LinkedIn](https://www.linkedin.com/company/attomdata)
- [GitHub Org](https://github.com/AttomDataSolutions)

## Maintainers

- Kin Lane — kin@apievangelist.com — [API Evangelist](https://apievangelist.com)
