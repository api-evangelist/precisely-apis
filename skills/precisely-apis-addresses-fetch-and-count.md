---
name: precisely-apis-addresses-fetch-and-count
description: Retrieve addresses for a given boundary and then obtain the count of those addresses.
api: openapi/precisely-apis-addresses-api-openapi.yml
operations:
- getAddressesbyBoundary
- getAddressesCountbyBoundary
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/precisely-apis-addresses-api-openapi.yml ; every operationId checked against the contract
---

# precisely-apis-addresses-fetch-and-count

Retrieve addresses for a given boundary and then obtain the count of those addresses.

## Steps

1. 1. Call `getAddressesbyBoundary` with the required request body fields for the boundary specification.
2. 2. Call `getAddressesCountbyBoundary` with the same boundary specification to obtain the total count.

## Rules

- Authentication: Include an OAuth2 password grant token in the `Authorization` header as `Bearer <token>`.
- Idempotency: Both POST endpoints are safe to retry as they do not modify server state.
