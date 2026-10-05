# TDI 0.1.0 conformance

## Brief Core

A Brief Core document:

1. Validates against `tdbs.schema.json`.
2. Uses only controlled vocabulary values defined by this release.
3. Contains one to five `ranked_intents` entries.
4. Uses contiguous ranks beginning at 1, with no duplicate rank or duplicate intent/role pair.
5. Orders ranked intentions by descending suitability score.
6. Includes at least one semantic layer directive.
7. Separates brief licensing from the rights of cited source material.
8. Contains no credentials, private endpoints, or user-identifying secrets.

## Library Brief

A Library Brief satisfies Brief Core and additionally:

1. Has a globally unique, stable `id` within the library.
2. Has a canonical name, expressive alias, genre, and era label.
3. Includes at least one evidence source with a rights statement.
4. Uses `review_status` of `reviewed` or `approved` before public release.
5. Includes a short preferred map credit.
6. Declares provider compilation status for all supported library targets.
7. Passes human review for attribution, cultural sensitivity, institutional affiliation wording, and implementability.

## Compiled Package

A Compiled Package is not itself a TDI brief. It must include:

- The source brief ID and cryptographic digest.
- TDI version.
- Provider and provider style-specification version.
- Source/template identifier and version.
- Compiler identifier and version.
- Compilation timestamp.
- Validation status and known limitations.
- Executable style resources and their licenses.

## Rules requiring a linter

JSON Schema does not enforce ordered scores, contiguous ranks, cross-field uniqueness, semantic layer presence, URL retrieval, source-license accuracy, or provider compatibility. The TDI linter is responsible for these checks.

## Compatibility

Readers must ignore unknown members only inside `extensions`. Unknown members elsewhere are validation errors. Extension keys should use a collision-resistant namespace such as `org.example.feature`.
