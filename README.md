# ATTOM (attomdata)

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/attomdata/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/attomdata/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Real Estate
- Property Data
- Property Intelligence
- Mortgage
- Assessment
- AVM
- Foreclosure
- Transactions
- Owner Data
- Building Permits
- Geospatial
- Boundaries
- Demographics
- Neighborhood
- POI
- Insurance
- Mortgage Technology
- PropTech

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### ATTOM Property API

Comprehensive property intelligence for 160M+ U.S. properties. Resources cover /property, /assessment, /assessmenthistory, /sale, /saleshistory, /salescomparables, /attomavm, /avm, /avmhistory, /rentalavm, /homeequity, /allevents, /school, /transportationnoise, /preforeclosure, and /property/buildingpermits, each available in `snapshot` and `detail` packages. Returns property characteristics, ownership and mortgage records, assessed values and tax history, sales history, AVM valuations (current and historical), rental AVM, home equity, school assignments, transportation noise, foreclosure status, and building permits. Inputs include AttomID, address, address1/address2, and geographic radius/bounding box.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/propertyapi/v1.0.0`

#### Tags

- Property
- Real Estate
- Assessment
- AVM
- Sales
- Mortgage
- Owner
- Building Permits
- Foreclosure

#### Properties

- [Documentation](https://api.developer.attomdata.com/docs)
- [OpenAPI](openapi/attom-property-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/attom-property-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/attom-property-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman](https://github.com/AttomDataSolutions/postman-collections) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [JSON Schema](json-schema/attom-property-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/attom-assessment-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/attom-sale-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/attom-avm-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/attomdata-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/attom-property-detail-example.json)

### ATTOM Area API

Area and boundary lookup for state, county, CBSA, neighborhood, school zone, ZIP, and other geographic units. Resources include /area/boundary/detail (GeoJSON boundary polygons), /area/hierarchy/lookup (geographic hierarchy for a lat/lon), /area/state/lookup, /area/county/lookup, /area/cbsa/lookup, /area/geoid/lookup, /area/geoId/legacyLookup, and the v4 /v4/location/lookup that resolves any geoIdV4 to its location metadata.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com/areaapi`

#### Tags

- Geography
- Boundary
- Parcel
- GeoID
- CBSA
- County
- State

#### Properties

- [Documentation](https://api.developer.attomdata.com/docs)
- [OpenAPI](openapi/attom-area-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/attom-area-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/attom-area-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/attom-area-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/attom-area-hierarchy-example.json)

### ATTOM POI API

Points of Interest search and category lookup across 120+ business categories — restaurants, banks, shopping, services, and more. Search by point (lat/lon + radius) or address; filter by category, line of business, and industry. Returns POIs with names, categories, distances, and addresses.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com`

#### Tags

- Points Of Interest
- Neighborhood
- Business
- Search

#### Properties

- [Documentation](https://api.developer.attomdata.com/docs)
- [OpenAPI](openapi/attom-poi-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/attom-poi-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/attom-poi-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/attom-poi-search-example.json)

### ATTOM Community API

Neighborhood-level community profile data including demographics, population, household income, crime indices, weather, commute, education, and quality-of-life metrics. Resources cover /v4.0.0/neighborhood/community (community profile by geoIdV4) and /v4/location/lookup for resolving locations by geoIdV4 and geography-type abbreviation (ZI, ND, CO, ST, etc.).

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com`

#### Tags

- Community
- Neighborhood
- Demographics
- Crime
- Weather
- Schools
- Location

#### Properties

- [Documentation](https://api.developer.attomdata.com/docs)
- [OpenAPI](openapi/attom-community-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/attom-community-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/attom-community-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/attom-community-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/attom-community-neighborhood-example.json)

### ATTOM Parcel Tiles API

Vector parcel tile service for rendering ATTOM parcel boundaries on web/mobile maps. Tile endpoints return styled parcel geometries suitable for Mapbox, MapLibre, and Leaflet integrations. Includes authentication via API key and per-zoom-level tile endpoints.

- **Human URL:** [https://api.developer.attomdata.com/docs](https://api.developer.attomdata.com/docs)
- **Base URL:** `https://api.gateway.attomdata.com`

#### Tags

- Parcel
- Tiles
- Mapping
- GeoJSON
- Vector Tiles

#### Properties

- [Documentation](https://api.developer.attomdata.com/docs)
- [OpenAPI](openapi/attom-parcel-tiles-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/attom-parcel-tiles-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/attom-parcel-tiles-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.attomdata.com/)
- [Developer Portal](https://api.developer.attomdata.com/)
- [Documentation](https://api.developer.attomdata.com/docs)
- [Documentation](https://api.developer.attomdata.com/docs/guides)
- [Sign Up](https://api.developer.attomdata.com/signup)
- [Login](https://api.developer.attomdata.com/login)
- [Documentation](https://www.attomdata.com/solutions/property-data-api/)
- [Documentation](https://www.attomdata.com/solutions/bulk-data-licensing/)
- [Documentation](https://www.attomdata.com/solutions/cloud-delivery/)
- [Documentation](https://www.attomdata.com/data/)
- [Blog](https://www.attomdata.com/news/most-recent/)
- [Documentation](https://www.attomdata.com/insights/white-papers/)
- [Documentation](https://www.attomdata.com/webinars/)
- [Documentation](https://www.attomdata.com/glossary/)
- [Support](https://www.attomdata.com/contact-us/)
- [LinkedIn](https://www.linkedin.com/company/attomdata)
- [Twitter](https://twitter.com/attomdata)
- [Facebook](https://www.facebook.com/attomdata)
- [Git Hub](https://github.com/AttomDataSolutions)
- [Postman](https://github.com/AttomDataSolutions/postman-collections) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [SDK](https://github.com/AttomDataSolutions/Sample_Code)
- [SDK](https://github.com/AttomDataSolutions/School_Sample_Code)
- [SDK](https://github.com/AttomDataSolutions/POI_Sample_Code)
- [SDK](https://github.com/AttomDataSolutions/Community_Sample_Code)
- [Contact Email](mailto:datacustomercare@attomdata.com)
- [Contact Phone](tel:+18004625125)
- [Plans](plans/attomdata-plans-pricing.yml)
- [Rate Limits](rate-limits/attomdata-rate-limits.yml)
- [Fin Ops](finops/attomdata-finops.yml)
- [Vocabulary](vocabulary/attomdata-vocabulary.yml)
- [Spectral Rules](rules/attomdata-rules.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
