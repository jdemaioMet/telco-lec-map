# Telco LEC Map

An interactive US map showing the main telecom carriers (LECs) by state, built for the MetTel team.

## What it does

- **Hover** over any state to see a quick preview of its main carriers
- **Click** a state to expand the full carrier list below the map
- **Filter** by carrier type: ILEC, CLEC, Cable, or Wireless
- **Search** by state name to jump directly to a state's carrier list

## Carrier types

| Color | Type | Description |
|-------|------|-------------|
| 🔵 Blue | ILEC | Incumbent Local Exchange Carrier (AT&T, Verizon, Frontier, Lumen) |
| 🟢 Green | CLEC | Competitive LEC (RCN, WOW, Grande, Brightspeed) |
| 🟠 Amber | Cable | Cable/MSO (Comcast, Charter/Spectrum, Cox, Altice) |
| 🟣 Purple | Wireless | Wireless carriers (Verizon, T-Mobile, AT&T Wireless) |

## Deployment

Deployed via [Vercel](https://vercel.com). Any push to `main` triggers an automatic redeployment.

## Updating carrier data

All carrier data lives in the `stateCarriers` object inside `index.html`. To add or update a carrier for a state, find the state entry and add an object with `name` and `type` fields:

```js
"Texas": [
  { name: "AT&T Texas", type: "ILEC" },
  { name: "Windstream", type: "ILEC" },
  // add new carrier here
]
```

## Related

- **Carrier Contacts Directory** — a companion HTML file with carrier rep contacts sourced from Outlook (`telco-carrier-contacts.html`)

---

Built with [D3.js](https://d3js.org) and [TopoJSON](https://github.com/topojson/topojson). Data reflects major carrier presence as of 2024–2025.
