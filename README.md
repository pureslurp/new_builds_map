# Oakland County New-Build Communities Map

An interactive map showing new-build communities in Oakland County, Michigan, from approximately 1996 to present.

## What's Included

The map displays communities in three categories:

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

Value estimates must include a labeled source in `value_source`. Missing fields are displayed as blank rather than estimated.

## Known Limitations

Some communities are not shown on the map because they did not produce an accepted geocode match:
- Forest Edge
- Meadows of Lyon
- Aspen Ridge
- The Townes at Main Street
- The Villas at Waldon Village
- Townes at Waldon Village
- Cattails Preserve

## Usage

Open `index.html` in a browser or host it as a static site.
