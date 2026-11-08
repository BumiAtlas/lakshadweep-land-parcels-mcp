# Lakshadweep Land Parcels MCP (Kavaratti)

Connect your AI assistant (Claude, ChatGPT, Cursor) to [BumiAtlas](https://bumiatlas.com) for land research in Lakshadweep through the Model Context Protocol (MCP).

- Survey and subdivision parcels on Kavaratti island from the Bharatmaps Lakshadweep cadastral layer, with each parcel's area in ares and m², and remarks (roads, quarters)
- Lookup by coordinates or by survey number
- Satellite and street map images of a parcel and its neighbours, labelled by survey number

Only Kavaratti is covered; the other islands aren't in the source. No owners.

## Connect

```
https://bumiatlas.com/mcp/lakshadweep
```

Add it as a custom connector in any MCP client and sign in with Google; no API key. Tools, examples and data notes: [bumiatlas.com/mcp-docs/lakshadweep](https://bumiatlas.com/mcp-docs/lakshadweep).

- **Claude:** Settings → Connectors → Add custom connector, paste the URL, then Connect.
- **ChatGPT:** Settings → Apps & Connectors → Advanced → Developer mode, then Create with the URL and OAuth authentication.

These are BumiAtlas's India tools, so parcels in the other loaded states can be looked up too.

## Tools

| Tool | Description |
|---|---|
| `IN_parcel_search` | Find parcels by `latitude, longitude`, ULPIN, or khasra/survey number with state and village; each result is the whole record, the boundary as GeoJSON on request |
| `IN_parcel_image` | Satellite or street map image of a parcel or point, with every parcel in view outlined and labelled with its khasra, survey or dag number |

## Example prompts

- *"Which survey plot is at 10.5626, 72.6369 on Kavaratti, and how big is it?"*
- *"Show a satellite image of the parcels around 10.5626, 72.6369."*

## Coverage

Kavaratti island only.

## Data source

Bharatmaps (NIC), Lakshadweep cadastral layer. Parcels from the state land-record portals, compiled by datameet / ramSeraph [indian_cadastrals](https://github.com/ramSeraph/indian_cadastrals) (CC0). A copy of public data for research, not a legal land record.
