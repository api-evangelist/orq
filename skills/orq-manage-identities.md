---
name: orq-manage-identities
description: Create, retrieve, update, list, and delete identities.
api: openapi/orq-openapi.json
operations:
- CreateIdentity
- RetrieveIdentity
- UpdateIdentity
- ListIdentities
- DeleteIdentity
generated: '2026-10-21'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/orq-openapi.json ; every operationId checked against the contract
---

# orq-manage-identities

Create, retrieve, update, list, and delete identities.

## Steps

1. 1. Use `CreateIdentity` with the request body fields defined for creating an identity.
2. 2. Use `RetrieveIdentity` with the path parameter `id` to get the newly created identity.
3. 3. Use `UpdateIdentity` with the path parameter `id` and the request body fields for updating the identity.
4. 4. Use `ListIdentities` with optional query parameters for pagination as defined in the contract.
5. 5. Use `DeleteIdentity` with the path parameter `id` to remove the identity.

## Rules

- Auth: Include the API key in the `Authorization` header as required by the ApiKey (http) scheme.
- Idempotency: `CreateIdentity` and `DeleteIdentity` support idempotent behavior when the same request is repeated.
- Pagination: `ListIdentities` may return paginated results; use the pagination parameters provided in the response to retrieve subsequent pages.
- Errors: The API returns standard HTTP error codes (e.g., 400, 401, 404, 500) with error details in the response body.
