# TDBS 0.1.0 controlled vocabulary

## Ranked intentions

Intent answers: **What job should the map perform?** It does not encode scale, platform, density, dimensionality, or historical appearance.

| ID | Definition |
|---|---|
| `reference` | General geographic orientation, feature lookup, and broad contextual reading. |
| `navigation` | Route following, movement planning, and wayfinding. Use `navigation_modes` to distinguish road, transit, pedestrian, cycling, nautical, and air use. |
| `thematic` | Communication of a geographic variable, category, relationship, or argument. `role: context` indicates a thematic underlay; `role: primary` indicates that thematic symbols are central. |
| `data-visualization` | Quiet geographic context for dense analytical overlays, usually with sparse or absent labels. |
| `outdoors-recreation` | Trails, parks, access, recreation, and field use. |
| `human-geography` | Settlements, boundaries, culture, population, political geography, and human networks. |
| `physical-environmental` | Hydrography, ecology, climate, land cover, and natural systems. |
| `terrain-relief` | Elevation, landform, contours, hillshade, bathymetry, and relief as the principal subject. |
| `editorial-narrative` | News, explanation, persuasion, annotation, and story-led mapping. |
| `operational-monitoring` | Live incidents, assets, logistics, status, and dashboard-oriented situational awareness. |
| `schematic-network` | Topology, routes, flows, or networks where geographic geometry may be intentionally simplified or distorted. |
| `educational-interpretive` | Teaching, heritage, visitor interpretation, public history, and exhibition use. |

## Map role

| ID | Definition |
|---|---|
| `context` | The style should remain subordinate to user data or another visual layer. |
| `primary` | The style itself carries the map's principal message or use. |
| `hybrid` | Context and primary content are intentionally balanced. |

## Scale domains

Scale labels describe viewing purpose rather than fixed denominators, because web maps vary by screen and latitude.

| ID | Typical scope |
|---|---|
| `global` | World, hemisphere, or continent. |
| `regional` | Multi-country, country, state/province, or broad landscape. |
| `local` | Metropolitan area, municipality, neighborhood, park, or detailed corridor. |
| `site` | Campus, facility, parcel, building complex, or very detailed operational area. |

## Additional facets

- `label_density`: `none`, `sparse`, `moderate`, `dense`
- `terrain_emphasis`: `none`, `context`, `primary`
- `dimensionality`: `2d`, `2.5d`, `3d`
- `interaction_fit`: `static`, `exploratory`, `operational`
- `navigation_modes`: `road`, `transit`, `pedestrian`, `cycling`, `nautical`, `air`
- `mobile_fit`: `low`, `moderate`, `high`
- `implementation_complexity`: `basic`, `intermediate`, `advanced`, `expert`
- `projection_bias`: `none`, `web-mercator`, `equal-area`, `conformal`, `local-planar`, `compromise`, `schematic`

## Suitability scoring

`score` ranges from 0 to 100 and represents the style's suitability for an intention, not aesthetic quality.

- 90–100: defining or exceptional use
- 75–89: strong use
- 60–74: useful with adaptation
- Below 60: omit from `ranked_intents`

Do not add weak intentions simply to reach five entries.

## Semantic layer visibility

- `required`: necessary to preserve the design or use intent
- `preferred`: should appear when the provider/source supports it
- `optional`: useful but safely omitted
- `suppress`: intentionally hidden or strongly de-emphasized

## Provider compilation status

- `verified`: compiled and validated against the named provider contract
- `limited`: compilable, but important design characteristics cannot be represented
- `unsupported`: no trustworthy executable output is currently available
- `not-tested`: no compilation attempt has been reviewed
