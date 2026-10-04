# NLGIS.ai Tile Design Brief Standard

## A shared language for designing tiled maps

**TDBS** — the **Tile Design Brief Standard** — is an open, provider-neutral format for describing how a map should look and behave before it becomes a provider-specific style.

It is designed to be useful to:

- map designers and cartographers;
- GIS professionals and software teams;
- prompt and research agents;
- tile-style libraries and compilers;
- anyone who wants to describe a map clearly without being locked into one provider.

> **Try it in TileStyler:** [www.tilestyler.com](https://www.tilestyler.com/)  
> Start from a reviewed brief or describe your own idea, then generate a unique design schema and provider-native style output.

## The simple idea

Write the durable design intent once. Compile it for the platform you need.

~~~
TDBS design brief
        +
provider source/template contract
        |
        v
MapTiler · ArcGIS Vector Tile Editor · Mapbox · MapLibre · other providers
~~~

A TDBS brief describes purpose, audience, scale, hierarchy, color, typography, linework, semantic layers, sources, rights, accessibility, and constraints. Provider-specific layer IDs, expressions, glyphs, sprites, and operational settings belong in the compilation stage.

## What is in this repository?

- tdbs/0.1.0/tdbs.schema.json — the normative JSON Schema.
- tdbs/0.1.0/vocabulary.json — controlled vocabulary for intentions and design concepts.
- tdbs/0.1.0/VOCABULARY.md — approachable definitions for people and agents.
- tdbs/0.1.0/CONFORMANCE.md — what it means for a brief or compiled package to conform.
- tdbs/0.1.0/examples/ — five historically grounded example briefs.
- docs/WORKFLOW.md — an authoring, research, compilation, and validation workflow.
- docs/EXAMPLES.md — notes about the included examples.
- LICENSE — Creative Commons Attribution 4.0 licensing.

## Why a design brief instead of only a style JSON?

A provider style JSON is an implementation artifact. It depends on a particular source, layer naming scheme, glyph endpoint, sprite package, expression language, and editor.

TDBS keeps the portable cartographic decision separate:

1. **Intent** — what the map is for.
2. **Design language** — how it should feel and communicate.
3. **Semantic layers** — what kinds of features should be styled.
4. **Evidence and rights** — where the ideas came from and how they may be used.
5. **Constraints** — what to preserve, avoid, test, or disclose.
6. **Provider compilation** — how that brief becomes an executable style.

This separation makes styles easier to compare, adapt, review, preserve, and translate.

## For people

You can author a brief in ordinary language. Describe:

- the geography and audience;
- the map’s purpose;
- the important layers;
- preferred scale and label density;
- visual character, colors, typography, and terrain;
- things the style must avoid;
- sources, attribution, and accessibility needs.

You do not need to know every provider’s internal layer name to express the design.

## For agents

Agents can use TDBS to:

1. filter a style library by ranked map intention;
2. select a suitable historical or contemporary design reference;
3. research and normalize a new brief;
4. preserve rights and attribution during transformation;
5. compile the same brief for a selected provider;
6. validate structure before spending time on rendering;
7. explain which parts are portable and which are provider-specific.

The controlled vocabulary and ranked intentions make mechanical selection possible before a model is asked to invent a style.

## For GIS software

A GIS application can treat a TDBS document as:

- a style-authoring input;
- a design handoff;
- a searchable library record;
- a provenance and attribution record;
- a provider-compilation source;
- a compatibility and validation target.

TDBS does not promise pixel-identical output across providers. It makes the intended design decisions explicit so differences can be documented rather than hidden.

## Included examples

The five examples are intentionally historical or institutionally grounded rather than based on contemporary technology companies:

1. Academic Cartography, Robinson School — Mid–Late 20th Century
2. French Cassini Survey — 18th Century
3. US County Atlas Landownership — 19th Century
4. US Fire Insurance Urban Atlas — 1880s–1950s
5. US WWII Newsmap — 1940s

They are interpretive briefs, not facsimiles or claims of endorsement. Review the sources and rights fields before using historical references in production work.

## Attribution and license

This repository uses **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

**Preferred attribution: CC – BY – NLGISLabs | WebMapper.org.**

See LICENSE for the complete terms. Where a brief identifies additional source lineage, preserve the source-specific attribution and rights information included in that brief.

## Project links

- [Use TileStyler](https://www.tilestyler.com/)
- [NLGIS.ai](https://www.nlgis.ai/)
- [NLGIS Labs](https://www.nlgislabs.com/)
- [WebMapper.org](https://www.webmapper.org/)
- [Prompt Cartography](https://www.promptcartography.com/)

TDBS 0.1.0 is an experimental foundation release. Contributions, critiques, examples, and implementation feedback are welcome.
