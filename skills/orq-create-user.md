---
name: orq-create-user
description: Create a new workspace user and verify its creation.
api: openapi/orq-openapi.json
operations:
- UserCreate
- UserGet
generated: '2026-10-21'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/orq-openapi.json ; every operationId checked against the contract
---

# orq-create-user

Create a new workspace user and verify its creation.

## Steps

1. 1. Call `UserCreate` with the required request body fields for a new user and include the ApiKey authentication header.
2. 2. Call `UserGet` with the `{id}` path parameter returned from the create call and include the ApiKey authentication header.

## Rules

- Authentication: Include an `ApiKey` header as defined by the provider.
- Pagination: Not applicable for this task.
- Idempotency: Not specified for these operations.
