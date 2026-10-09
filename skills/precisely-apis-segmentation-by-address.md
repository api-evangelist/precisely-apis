---
name: precisely-apis-segmentation-by-address
description: Retrieve segmentation data for a given address and then fetch advanced demographics for the same location.
api: openapi/precisely-apis-segmentation-api-openapi.yml
operations:
- getSegmentationByAddress
- getDemographicsAdvanced
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/precisely-apis-segmentation-api-openapi.yml ; every operationId checked against the contract
---

# precisely-apis-segmentation-by-address

Retrieve segmentation data for a given address and then fetch advanced demographics for the same location.

## Steps

1. 1. Call `getSegmentationByAddress` with the required address query parameters.
2. 2. Call `getDemographicsAdvanced` with the location identifiers returned from the previous step.

## Rules

- Auth: Include an OAuth2 password flow bearer token in the `Authorization` header.
- Idempotency: Both endpoints are safe to retry as they are GET/POST read‑only operations.
