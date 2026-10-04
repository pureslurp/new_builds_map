# Oakland County New-Build Communities Map

An interactive map showing new-build communities in Oakland County, Michigan, from approximately 1996 to present.

## What's Included

The map displays communities from multiple builders including Pulte, Del Webb, Toll Brothers, D.R. Horton, M/I Homes, Lombardo, and Robertson Homes.

Communities are organized in categories:

- **Built, single-family** — Single-family homes
- **Built, attached or condo** — Townhomes, villas, condos, and duplexes
- **Still selling** — Active communities

## Files

- `index.html` — Interactive Leaflet map with community pins
- `communities.csv` — Community data with location, type, and optional details
- `map-roads.png` — Static map snapshot

## Data Schema

The `communities.csv` file includes these columns:

**Required columns:**
- `name` — Community name
- `group` — Category (see above)
- `product` — Product description
- `lat`, `lon` — Coordinates
- `geocode_query` — Query used to obtain coordinates
- `display_name` — Geocode result display name

**Optional columns:**
- `builder` — Builder name (enables builder filter when populated)
- `home_type` — Type: single-family, condo, townhome, etc.
- `year_built` — Year of construction
- `value_estimate` — Typical home value estimate (numeric)
- `value_source` — Source for value estimate (e.g., "Zestimate", "recent comps")

The map includes builder and city filters that can be used together; cities are extracted from the `display_name` field. Value estimates must include a labeled source in `value_source`. Missing fields are displayed as blank rather than estimated.

## Usage

Open `index.html` in a browser or host it as a static site.
