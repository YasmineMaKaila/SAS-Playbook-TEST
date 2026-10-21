# SAS Pod Playbook

An interactive quick-reference for Screening and Applications (SAS) associates who
cover another market, transfer between markets, or need a fast refresher. It is a
**performance-support resource** — it supplements, and does not replace, the SAS
Standard Workflow Manual or formal SAS training.

## What's in this folder

```
sas-pod-playbook/
├── index.html    # the complete application (one self-contained file)
├── .nojekyll     # tells GitHub Pages to serve the file as-is
└── README.md     # this file
```

`index.html` embeds all of its own images (Cortland logo, LXD mark, illustration).
No build step, server, or database is needed.

## Publishing to GitHub Pages

1. Create a repository and add these three files to its root.
2. **Settings → Pages**, choose the branch and the root folder, then Save.
3. The site appears at `https://<org-or-user>.github.io/<repo-name>/`.

**Privacy — decide this before publishing.** A GitHub Pages site is reachable by
anyone with the link, even when the repository itself is private (unless your
GitHub plan includes Pages access control — ask your GitHub administrator). The
playbook contains SAS operational content (fees, concessions, screening rules)
and property addresses. If it should not be public, host it somewhere
access-controlled instead; the file works on any static host.

## What the page needs from the internet

| Dependency | Used for | If it's blocked |
|---|---|---|
| Google Fonts | Poppins / Inter typefaces | Page works with fallback fonts |
| `www.google.com/maps` (keyless embed) | The property map | Map area stays blank; the property name and address still show as text |
| `cortland.com` links | "View on Cortland.com" link under each address | Link just won't open |

Nothing is loaded from local paths, temporary URLs, or development servers.

### About the map (read this)

The map is a Google Maps iframe built directly from each property's approved
address — no coordinates are stored or needed. It uses Google's **keyless embed
format** (`https://www.google.com/maps?q=ADDRESS&output=embed`). That format is
not part of Google's officially documented Embed API, so Google could change or
restrict it without notice. If the map ever stops loading, edit the single
function `buildGoogleMapsEmbedUrl` in `index.html` — for example to Google's
keyed `maps/embed/v1/place` endpoint (requires an API key) or to a
stored-coordinate Leaflet/OpenStreetMap map. Google's default marker is used;
a custom Cortland pin cannot be placed inside Google's iframe.

The "View on Cortland.com" links were built from the pattern
`https://cortland.com/apartments/<property-name>/`. Two were opened and verified
individually (Cortland Duluth, Cortland at the Village); the rest follow the same
pattern but were not individually opened, so a few may not resolve.

## Sources of truth

| What | Authority |
|---|---|
| Operational content (fees, policies, procedures, property-specific exceptions) | `SAS Playbook Info 2026.docx` |
| Market names, official property names, property addresses | `APPROVED_SAS_PROPERTY_NAMES_AND_ADDRESSES.xlsx` |
| Page design | The approved landing-page and pod-page templates |

This page is a presentation layer. If it ever disagrees with the Word document,
the Word document governs — report the difference rather than editing the page.

## How the data is organised (inside `index.html`)

- **`PODS`** — one object per market. `id` is a stable internal key used by code,
  search, and element IDs. `displayName` is what learners see (no pod numbers).
  The old label (e.g. "GA Pod 1") is kept only as a hidden search alias.
  `sections` = General Pod Information; `propertyExceptions` = SAS-source details
  that apply to one community only.
- **`ROSTER_DATA.rosters`** — the approved property list for each market
  (`sourceName`, `displayName`, `streetAddress`, `city`, `state`, `zip`,
  `cortlandPropertyUrl`). A roster property appears in the selector and on the
  map **whether or not** it has a SAS exception. `exceptionSectionId` links a
  property to its exception when one exists.
- **`ROSTER_DATA.badges`** — the state abbreviation(s) in each market's circle,
  derived from the states of that market's own approved properties.
- A SAS exception whose community is **not** in the address spreadsheet is still
  shown, as its own entry in the property list with no address and a
  "Location pending approved address confirmation" map message — it is never
  hidden.

### Updating content

1. Edit the relevant object in `PODS` (operational text) or `ROSTER_DATA`
   (names/addresses), preserving source wording exactly.
2. Update `meta.sourceRefreshedDate` for the pod.
3. Leave `meta.humanVerifiedDate` / `verifiedBy` blank until an authorized SAS
   reviewer signs off — a refresh is not a verification.
4. Anything unclear in a source: keep it as written and add it to that pod's
   `reviewFlags` (never shown to learners).

## Open items needing a human decision

- **Virginia has no sheet in the address spreadsheet.** Its four listed properties
  (Cortland Pentagon City, at National Landing, Arlington, Rosslyn) were identified
  by their Virginia addresses, found on the Ohio & Tennessee sheet. "Virginia" as
  the market name is also unconfirmed. Please confirm both.
- **No approved address** (so no map; exception text still shown where one exists):
  Cortland McLean; Cortland Columbia Pike & Cortland on Pike.
- **Named in the SAS source but not found in the spreadsheet at all:** The Point at
  Stockbridge, Lake' Edge, Sugarland (likely "Sugar Land"), Las Casas.
- **One Central Fort Worth property is listed in the spreadsheet only as "3700"**
  (a street number, not a name). Shown with a "name needs review" note.
- **Bayport** is one property in the SAS source but two in the spreadsheet (North
  and South, different addresses). Both appear and both show the same exception.
- **Cortland at the Village:** the spreadsheet's address field was garbled; the
  address shown comes from the property's own cortland.com page.
- **"HASA"** is the market name exactly as the spreadsheet labels it; confirm
  whether a fuller market name was intended.

The spreadsheet's tab groupings do not line up one-to-one with the SAS pods (for
example, Virginia properties sit on the Ohio & Tennessee tab, and it also lists
Illinois and Alabama properties that belong to no SAS pod; those are excluded).

## Version

v2 — approved visual design, state-abbreviation badges, full property rosters,
address-based property maps. All 11 markets. Built October 2026.
