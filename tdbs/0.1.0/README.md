# Tile Design Brief Standard (TDBS) 0.1.0

TDBS is a provider-neutral interchange format for describing the visual intent of tiled and web maps. A TDBS document is a design brief, not an executable renderer stylesheet.

## Design principles

1. Preserve cartographic intent independently of any provider schema.
2. Keep purpose, map role, scale, dimensionality, density, and interaction as separate dimensions.
3. Express design decisions through semantic layer families rather than provider layer IDs.
4. Preserve evidence, provenance, accessibility requirements, limitations, and source-specific rights.
5. Make deterministic filtering possible before any model is called.
6. Permit extensions without allowing unnamespaced fields to silently change the core format.

## Package contents

- tdbs.schema.json — normative JSON Schema Draft 2020-12 validation schema.
- vocabulary.json — machine-readable controlled vocabulary.
- VOCABULARY.md — human-readable definitions and selection guidance.
- CONFORMANCE.md — conformance levels and validation rules.
- examples/ — five historically grounded example briefs.
- LICENSE.md — licensing and attribution.

## Core versus compiled artifacts

A conforming TDBS brief does not contain provider source URLs, provider layer IDs, API keys, sprites, glyph endpoints, or executable expressions unless they appear in a namespaced extension. Those operational details belong in compiled packages and their manifests.

## Versioning

spec_version uses semantic versioning. Patch releases clarify wording or fix validation defects; minor releases add backward-compatible vocabulary or fields; major releases may rename, remove, or reinterpret fields.

A document must declare the exact version against which it was authored.

## Status

Experimental foundation release.
