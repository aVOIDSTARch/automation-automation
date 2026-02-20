# Minimum Core Schema (Copilot)

This is a compact, pragmatic starting schema for the `NODE`-`ACTION`-`RESOURCE` model. Keep the core small and extensible.

## JSON Schema (conceptual)

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "MinimalNode",
  "type": "object",
  "required": ["id","schema_version","paradigm","metadata","actions","resources"],
  "properties": {
    "id": {"type":"string","description":"Canonical node identifier (URI-like)"},
    "schema_version": {"type":"string","description":"Semantic version of node schema"},
    "paradigm": {"type":"string","description":"INTERNET | REAL_WORLD | other"},
    "domain": {"type":"string","description":"Optional domain scope"},
    "metadata": {
      "type":"object",
      "properties": {
        "title": {"type":"string"},
        "description": {"type":"string"},
        "location": {"type":"object","description":"Address, IP, or geo coordinates"}
      }
    },
    "actions": {
      "type":"array",
      "items": {
        "type":"object",
        "required":["id","title","inputs","outputs","semantics"],
        "properties":{
          "id": {"type":"string"},
          "title": {"type":"string"},
          "description": {"type":"string"},
          "inputs": {"type":"object"},
          "outputs": {"type":"object"},
          "semantics": {"type":"object","properties":{
            "idempotent": {"type":"boolean"},
            "safe": {"type":"boolean"},
            "async": {"type":"boolean"}
          }}
        }
      }
    },
    "resources": {
      "type":"array",
      "items":{
        "type":"object",
        "required":["id","type"],
        "properties":{
          "id": {"type":"string"},
          "type": {"type":"string","description":"string|number|geo|json|binary"},
          "description": {"type":"string"},
          "access": {"type":"object","description":"Access metadata and default visibility"}
        }
      }
    },
    "permissions": {"type":"object","description":"Optional capability/ACL metadata"}
  }
}
```

## Minimal example (node manifest)

```json
{
  "id": "urn:copilot:node:store:coffee-shop-42",
  "schema_version": "1.0.0",
  "paradigm": "REAL_WORLD",
  "domain": "local-retail",
  "metadata": {
    "title": "Corner Coffee Shop",
    "description": "Small coffee shop with pickup window",
    "location": {"lat":40.7128,"lon":-74.0060}
  },
  "actions": [
    {
      "id":"order_coffee",
      "title":"Order Coffee",
      "description":"Place a pickup order",
      "inputs": {"type":"object","properties":{"drink":{"type":"string"},"size":{"type":"string"}}},
      "outputs": {"type":"object","properties":{"order_id":{"type":"string"},"eta_minutes":{"type":"number"}}},
      "semantics": {"idempotent":false,"safe":false,"async":true}
    }
  ],
  "resources": [
    {"id":"menu_v1","type":"json","description":"Current menu and prices"}
  ],
  "permissions": {"default":"kiosk-only","scopes":[]}
}
```

## Notes & guidance
- Identification: use URN/URI-like IDs to allow pluggable resolution (e.g., `urn:`, `https:`).
- Keep action inputs/outputs as JSON Schemas for compatibility with existing tooling.
- Security: design for scopes/capabilities in `permissions`; prefer short-lived, signed capability tokens for delegation.
- Discovery: start with domain-scoped registries (simple catalogs) before attempting federation.
- Granularity: prefer resource-per-record or resource-per-entity rather than per-field to avoid identifier explosion.
- Semantics flags (`idempotent`, `safe`, `async`) help orchestration engines reason about retries and composition.

If you'd like, I can generate a small reference HTTP adapter that serves this manifest and an example client that discovers and calls `order_coffee`.
