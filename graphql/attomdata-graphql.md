# ATTOM Data GraphQL Schema

Conceptual GraphQL schema for the ATTOM Property Intelligence API suite, covering
160M+ U.S. properties across property characteristics, assessment, sales history,
mortgage and lien data, foreclosure status, owner information, AVM valuations,
schools, building permits, community demographics, crime, hazards, POI, and geographic
area boundaries.

## Provider

- **Name:** ATTOM Data
- **Developer Portal:** https://api.developer.attomdata.com/
- **Base REST API:** https://api.gateway.attomdata.com/propertyapi/v1.0.0
- **Authentication:** API key via `apikey` HTTP header

## Schema File

[attomdata-schema.graphql](attomdata-schema.graphql)

## Root Query Operations

| Operation | Description |
|---|---|
| `property` | Single property lookup by AttomID, address, or APN |
| `propertySearch` | Spatial search by radius or bounding box |
| `assessment` | Current assessment snapshot |
| `assessmentHistory` | Multi-year assessment history |
| `sale` | Most recent sale record |
| `salesHistory` | All sales for a property |
| `salesComparables` | Comparable sales near a property |
| `avm` | Current AVM valuation |
| `avmHistory` | Historical AVM estimates |
| `rentalAvm` | Rental AVM estimate |
| `homeEquity` | Home equity estimate |
| `foreclosure` | Pre-foreclosure / foreclosure status |
| `buildingPermits` | Building permit history |
| `allEvents` | All event types in a single query |
| `schools` | School assignments for an address |
| `transportationNoise` | Transportation noise index |
| `poi` | Points of Interest near a lat/lon |
| `community` | Neighborhood profile by geoIdV4 |
| `areaBoundary` | GeoJSON boundary polygon |
| `areaHierarchy` | Geographic hierarchy for a lat/lon |
| `counties` | County list for a state |
| `locationLookup` | Resolve geoIdV4 to location metadata |

## Named Types (65)

### Property Core
- `Property` — root property object with all sub-resources
- `PropertyDetails` — summary characteristics (beds, baths, sqft, year built)
- `PropertyType` — enum: SINGLE_FAMILY, CONDO, TOWNHOUSE, MULTI_FAMILY, etc.
- `PropertyAddress` — full address with geocoordinates
- `PropertyIdentifiers` — AttomID, APN, FIPS, geoIdV4, census fields
- `PropertySearchResult` — paginated property search response

### Identifiers
- `APN` — assessor parcel number (raw, formatted, original)
- `FIPS` — state + county FIPS codes
- `ATTOMID` — represented as the `ID` scalar on `Property.attomId`

### Building / Lot
- `Building` — detailed building characteristics
- `GarageDetails` — garage type, spaces, area
- `BasementDetails` — basement type, area, finished status
- `RoofDetails` — roof type and material
- `ConstructionDetails` — frame, exterior walls, foundation
- `Lot` — lot size, depth, frontage, zoning, land use

### Assessment
- `Assessment` — annual assessment record
- `AssessmentDetails` — jurisdiction, year, filing date, values
- `AssessedValue` — total, improvement, land assessed values
- `MarketValue` — total, improvement, land market values
- `Improvement` — improvement value and percentage
- `Land` — land value, acres, square feet
- `TaxDetails` — tax amount, year, delinquent year
- `ExemptionType` — enum: HOMESTEAD, SENIOR, VETERAN, DISABILITY, etc.

### Deed
- `Deed` — deed document linking buyer, seller, and mortgage
- `DeedDetails` — document type, recording date, document number
- `TransferDate` — structured date (year, month, day)
- `Buyer` — buyer name, address, ownership rights
- `Seller` — seller name and address

### Mortgage
- `MortgageDetails` — loan amount, lender, lien type, rate, term
- `Lender` — lender name, code, type, address
- `LienType` — enum: FIRST, SECOND, THIRD, HELOC, OTHER
- `LienAmount` — amount and currency

### Sales
- `Sale` — sale record with deed and mortgage
- `SaleDetails` — sale and recording dates, distressed/REO flags
- `SaleDate` — structured sale date
- `SalePrice` — amount, currency, sale code
- `SaleType` — enum: ARMS_LENGTH, REO, SHORT_SALE, FORECLOSURE, etc.

### Foreclosure
- `Foreclosure` — full foreclosure record
- `ForeclosureDetails` — default amount, recording date, jurisdiction
- `ForeclosureStage` — enum: PRE_FORECLOSURE through REO / REDEEMED
- `ForeclosureDate` — default, recording, auction, REO dates

### Listing
- `Listing` — property listing with agent and broker
- `ListingDetails` — MLS ID, description, virtual tour URL
- `ListingStatus` — enum: ACTIVE, PENDING, SOLD, EXPIRED, etc.
- `ListPrice` — amount, currency, price per sqft
- `Agent` — agent contact and license details
- `Broker` — brokerage contact details

### Owner
- `Owner` — owner record with details and mailing address
- `OwnerDetails` — owner names, type, trust/corporate name
- `OwnerAddress` — owner mailing address with match code
- `Occupancy` — enum: OWNER_OCCUPIED, TENANT_OCCUPIED, VACANT, etc.

### Schools
- `School` — school with rating, district, and contact info
- `SchoolDetails` — name, phone, website, NCES ID
- `SchoolRating` — GreatSchools rating, parent rating, test scores
- `SchoolDistrict` — district name, NCES district ID, address
- `SchoolType` — enum: ELEMENTARY through CHARTER/MAGNET

### POI
- `POI` — point of interest with distance and contact
- `POIDetails` — name, category, SIC/NAICS codes, chain name
- `POIType` — enum: RESTAURANT, BANK, RETAIL, HEALTHCARE, etc.

### Community / Demographics
- `Community` — neighborhood profile by geoIdV4
- `CommunityDetails` — city, county, population, median home value, walk/transit scores
- `Demographics` — full demographics container
- `DemographicsDetails` — age, income, poverty, unemployment
- `Income` — median and per-capita income with distribution
- `PopulationDetails` — total, growth rate, density, age and race distribution

### Crime
- `Crime` — crime data container
- `CrimeDetails` — violent, property, total counts and rates by year
- `CrimeIndex` — indexed scores vs. national baseline

### Hazards
- `HazardDetails` — flood, noise, earthquake, wildfire, hurricane, hail, wind, tornado
- `FloodZone` — FEMA zone, FIRM panel, SFHA flag

### Permits
- `Permit` — building permit record
- `PermitDetails` — permit number, type, status, dates, cost, contractor

### Valuation (HVA)
- `HVA` — valuation estimate (AVM, rental AVM, home equity)
- `HVAAmount` — value with high/low/mid range
- `HVACalcDetails` — model, confidence score, forecast std dev
- `HVAEstimateDetails` — type, price per sqft, rent, yield, cap rate
- `ValuationType` — enum: AVM, RENTAL_AVM, HOME_EQUITY, OPINION

### Events / Area / Auth
- `AllEvents` — union of all event types for a property
- `AreaBoundary` — GeoJSON boundary string for a geographic unit
- `AreaHierarchy` — full geographic hierarchy for a coordinate
- `AreaUnit` — individual geographic unit (geoId, geoIdV4, name, type)
- `APIKey` — API key metadata with rate limit counters
- `Token` — OAuth-style token (for future use)

## Authentication

ATTOM APIs authenticate via an API key sent as the `apikey` request header. Obtain
a key through the [30-day free trial signup](https://api.developer.attomdata.com/signup).
The `APIKey` and `Token` types in this schema represent the key metadata returned by
account management endpoints.

## Coverage

This schema maps to the following ATTOM REST endpoints:

- `/propertyapi/v1.0.0/property/detail` — `property` query
- `/propertyapi/v1.0.0/property/snapshot` — `propertySearch` query
- `/propertyapi/v1.0.0/assessment/detail` — `assessment` query
- `/propertyapi/v1.0.0/assessmenthistory/detail` — `assessmentHistory` query
- `/propertyapi/v1.0.0/sale/detail` — `sale` query
- `/propertyapi/v1.0.0/saleshistory/detail` — `salesHistory` query
- `/propertyapi/v1.0.0/salescomparables/detail` — `salesComparables` query
- `/propertyapi/v1.0.0/attomavm/detail` — `avm` query
- `/propertyapi/v1.0.0/avmhistory/detail` — `avmHistory` query
- `/propertyapi/v1.0.0/rentalavm/detail` — `rentalAvm` query
- `/propertyapi/v1.0.0/homeequity/detail` — `homeEquity` query
- `/propertyapi/v1.0.0/allevents/detail` — `allEvents` query
- `/propertyapi/v1.0.0/school/snapshot` — `schools` query
- `/propertyapi/v1.0.0/transportationnoise/snapshot` — `transportationNoise` query
- `/propertyapi/v1.0.0/preforeclosure/detail` — `foreclosure` query
- `/propertyapi/v1.0.0/property/buildingpermits` — `buildingPermits` query
- `/areaapi/v4/location/lookup` — `locationLookup` query
- `/areaapi/area/boundary/detail` — `areaBoundary` query
- `/areaapi/area/hierarchy/lookup` — `areaHierarchy` query
- `/v1/neighborhood/poi` — `poi` query
- `/v4.0.0/neighborhood/community` — `community` query
