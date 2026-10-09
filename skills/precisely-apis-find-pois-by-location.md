---
name: precisely-apis-find-pois-by-location
description: Find points of interest near a location and retrieve detailed information for a selected POI.
api: openapi/precisely-apis-places-api-openapi.yml
operations:
- getPOIsByLocation
- getPOIById
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/precisely-apis-places-api-openapi.yml ; every operationId checked against the contract
---

# precisely-apis-find-pois-by-location

Find points of interest near a location and retrieve detailed information for a selected POI.

## Steps

1. 1. Call `getPOIsByLocation` with query parameters `latitude`, `longitude`, and optional `radius` as defined in the contract.
2. 2. From the returned list, select a POI and call `getPOIById` with the path parameter `id` of the chosen POI.

## Rules

- Auth: Include an OAuth2 password flow bearer token in the `Authorization` header.
- Errors: The API returns standard HTTP error codes; on rate‑limit exhaustion no specific limit is defined.
