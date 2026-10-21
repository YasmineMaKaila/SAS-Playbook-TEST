# SAS Pod Playbook — Naming + Address Reconciliation Table

**Source of authority for this pass:** APPROVED_SAS_PROPERTY_NAMES_AND_ADDRESSES.xlsx (market names, official property names, addresses). The SAS Playbook Info 2026.docx remains the sole authority for operational content — nothing in this pass touched fees, policies, or procedures.

## Part 1 — Pod-Level Market Names

| Internal Pod ID | Current/Legacy UI Label (kept as hidden search alias) | Approved Market Name (now displayed) | Sourced From Spreadsheet? |
|---|---|---|---|
| `ga1` | GA Pod 1 | **Georgia** | Yes — sheet tab "Georgia Pod" |
| `nc3` | NC Pod 3 | **North Carolina** | Yes — sheet tab "North Carolina Pod" |
| `nfl4` | North Fl Pod 4 | **North Florida** | Yes — sheet tab "North Florida Pod" |
| `sfl6` | South Fl Pod 6 | **South Florida** | Yes — sheet tab "South Florida Pod" |
| `ohtn7` | OH/TN Pod 7 | **Ohio & Tennessee** | Yes — sheet tab "Ohio & Tennessee Pod" |
| `va8` | Pod 8 VA | **Virginia** | **No — spreadsheet has no Virginia/Pod 8 sheet.** "Virginia" is a flagged fallback derived from the existing SAS source's own "VA" abbreviation, not from the approved spreadsheet. |
| `dallas9` | Pod 9 North Dallas | **North Dallas** | Yes — sheet tab "North Dallas Pod" |
| `cfw10` | CFW Pod 10 | **Central Fort Worth** | Yes — sheet tab "Central Fort Worth Pod" |
| `hasa11` | HASA Pod 11 | **HASA** | Yes — sheet tab "HASA Pod" |
| `mwp12` | Pod 12 Mountain West | **Mountain West** | Yes — sheet tab "Mountain West Pod" |
| `az13` | Pod 13: AZ | **Arizona** | Yes — sheet tab "Arizona Pod" |

**Flag:** Pod 8 (Virginia) has no corresponding sheet anywhere in the approved spreadsheet. "Virginia" is displayed as a reasonable placeholder, but is NOT yet an approved spreadsheet-sourced market name. Needs your explicit confirmation, or an added sheet.

**Note on "HASA":** the spreadsheet itself labels this pod's tab "HASA Pod" with no separate state/market name — HASA appears to be an internal program/team acronym rather than a geographic market. Displayed as "HASA" since that's exactly what the approved sheet says, but flagging in case a fuller market name (e.g. a specific Houston-area label) was intended instead.

## Part 2 — Property-Level Reconciliation (existing Property-Specific Information dropdowns)

| Pod (Market) | SAS Source Property Name | Approved Display Name | Name Verified? | Approved Address | Ready for Map? |
|---|---|---|---|---|---|
| Georgia | Duluth Property | **Cortland Duluth** | Yes — applied to live interface | Cortland Duluth: 1335 Herrington Rd, Duluth, GA 30096 | Yes* |
| Georgia | The Village | **Cortland at the Village** | Yes — applied to live interface | Cortland at the Village: Lake Park Gate** | No — address incomplete |
| North Carolina | Cortland Cary | **Cortland Cary** | Yes — applied to live interface | Cortland Cary: 5110 Alston Glen Drive, Cary, NC 27519 | Yes* |
| North Carolina | Midtown East | **Cortland Midtown East** | Yes — applied to live interface | Cortland Midtown East: 2601 Noblewood Circle, Raleigh, NC 27604 | Yes* |
| North Carolina | University City | **Cortland University City** | Yes — applied to live interface | Cortland University City: 1421 Baseline Rd, Charlotte, NC 28262 | Yes* |
| North Florida | Bayport | *(not applied — see flag)* | Ambiguous — Cortland Bayport North: 10150 Parkers Landing Dr, Tampa, FL 33615; Cortland Bayport South: 10510 Parkers Landing Dr, Tampa, FL 33615 | multiple | No |
| North Florida | Satori | **Cortland Satori** | Yes — applied to live interface | Cortland Satori: 3110 Grand Ave., Pinellas Park, FL 33782 | Yes* |
| North Florida | Bowery | **Cortland Bowery** | Yes — applied to live interface | Cortland Bowery: 6301 S West Shore Blvd, Tampa, FL 33616 | Yes* |
| North Florida | Brighton Bay | **Cortland Brighton Bay** | Yes — applied to live interface | Cortland Brighton Bay: 10901 Brighton Bay Blvd NE, St. Petersburg, FL 33716 | Yes* |
| North Florida | Bermuda Lake | **Cortland Bermuda Lake** | Yes — applied to live interface | Cortland Bermuda Lake: 2648 Bermuda Lake Dr, Brandon, FL 33510 | Yes* |
| South Florida | Midtown Miami | **Cortland Midtown Miami** | Yes — applied to live interface | Cortland Midtown Miami: 2901 NE 1st Ave, Miami, FL 33137 | Yes* |
| South Florida | Hammocks | **Cortland at the Hammocks** | Yes — applied to live interface | Cortland at the Hammocks, Phase 1: 15280 SW 104th St Miami, FL 33196<br>Cortland at the Hammocks, Phase 2: 15000 SW 104th St Miami, FL 33196 | Needs SME decision (see flag) |
| South Florida | South Kendall | **Cortland South Kendall** | Yes — applied to live interface | Cortland South Kendall: 15520 SW 127th Ave, Miami, FL 33177 | Yes* |
| South Florida | Portofino Place | **Cortland Portofino Place** | Yes — applied to live interface | Cortland Portofino Place: 4400 Portofino Way, West Palm Beach, FL 33409 | Yes* |
| South Florida | Hollywood | **Cortland Hollywood** | Yes — applied to live interface | Cortland Hollywood: 2300 N 29th Avenue, Hollywood, FL 33020 | Yes* |
| South Florida | Pembroke Pines | **Cortland Pembroke Pines** | Yes — applied to live interface | Cortland Pembroke Pines: 8530 SW 1st St, Pembroke Pines, FL 33025 | Yes* |
| Ohio & Tennessee | Cortland New Albany & Dublin | **Cortland at New Albany & Cortland Dublin** | Yes — applied to live interface | Cortland at New Albany: 5185 Sulgrave Drive, New Albany, OH 43054<br>Cortland Dublin: 5284 Avery Rd., Dublin, OH 43016 | Needs SME decision (see flag) |
| Ohio & Tennessee | Hilliard | **Cortland Hilliard** | Yes — applied to live interface | Cortland Hilliard: 2581 Walcutt Rd, Hilliard, OH 43026 | Yes* |
| Ohio & Tennessee | Northlake | **Cortland Northlake** | Yes — applied to live interface | Cortland Northlake: 7205 Northlake Summit Dr, Sunbury, OH 43074 | Yes* |
| Ohio & Tennessee | Powell | **Cortland Powell** | Yes — applied to live interface | Cortland Powell: 3400 Club Way Ct, Powell, OH 43065 | Yes* |
| Ohio & Tennessee | Sunbury | **Cortland Sunbury** | Yes — applied to live interface | Cortland Sunbury: 2199 Rushmore Lane, Sunbury, OH 43074 | Yes* |
| Ohio & Tennessee | Bend at Broad | **The Bend at Broad** | Yes — applied to live interface | The Bend at Broad: 170 Heatherbridge Lane, Blacklick, OH 43004 | Yes* |
| Ohio & Tennessee | Cortland at the Nations | **Cortland at The Nations** | Yes — applied to live interface | Cortland at The Nations: 4731 Centennial Blvd., Nashville, TN 37209 | Yes* |
| Virginia | Cortland McLean | — | **NOT VERIFIED** — no match in approved spreadsheet | — | No |
| Virginia | Pentagon City | **Cortland Pentagon City** | Yes — applied to live interface | Cortland Pentagon City: 1221 S Eads St, Arlington, VA 22202 | Yes* |
| Virginia | Cortland Columbia Pike & Cortland on Pike | — | **NOT VERIFIED** — no match in approved spreadsheet | — | No |
| North Dallas | Cortland Legacy | **Cortland Legacy** | Yes — applied to live interface | Cortland Legacy: 5275 Town and Country Blvd, Frisco, TX 75034 | Yes* |
| North Dallas | Cortland Prairie Creek | **Cortland Prairie Creek** | Yes — applied to live interface | Cortland Prairie Creek: 3560 Alma Road, Richardson, TX 75080 | Yes* |
| North Dallas | Cortland at Castle Hills | **Cortland Castle Hills** | Yes — applied to live interface | Cortland Castle Hills: 2040 E State Hwy 121 BUS, Lewisville, TX 75056 | Yes* |
| North Dallas | Stonebriar | **Cortland at Stonebriar** | Yes — applied to live interface | Cortland at Stonebriar: 3100 Ohio Dr, Frisco, TX 75035 | Yes* |
| North Dallas | Cortland Preston North | **Cortland Preston North** | Yes — applied to live interface | Cortland Preston North: 9440 Stratton Dr, Frisco, TX 75035 | Yes* |
| Central Fort Worth | Cortland M-Line | **M-Line** | Yes — applied to live interface | M-Line: 3200 McKinney Ave, Dallas, TX 75204 | Yes* |
| Central Fort Worth | Water's Edge | **Waters Edge** | Yes — applied to live interface | Waters Edge: 1701 Royal Lane, Farmers Branch, TX 75229 | Yes* |
| Central Fort Worth | Chisholm Trail | **Chisholm Trail** | Yes — applied to live interface | Chisholm Trail: 9100 Summit Ridge, Fort Worth, TX 76123 | Yes* |
| Central Fort Worth | Ridglea | **Ridglea** | Yes — applied to live interface | Ridglea: 3601 Westridge Ave, Fort Worth, TX 76116 | Yes* |
| HASA | Museum District | **Museum District** | Yes — applied to live interface | Museum District: 5280 Caroline Street, Houston, TX 77004 | Yes* |

\* "Ready" means an approved full street address exists. Actual map/pin construction has not started — that remains a separate, later step per your required order of work.

## Flags requiring your explicit confirmation

1. **Pod 8 / Virginia has no spreadsheet sheet at all.** "Virginia" is a placeholder pending your confirmation or an added sheet.
2. **Cortland McLean** (Virginia) — no matching entry found anywhere in the approved spreadsheet. Left unchanged in the interface.
3. **Cortland Columbia Pike & Cortland on Pike** (Virginia) — no matching entry found anywhere in the approved spreadsheet, individually or combined. Left unchanged.
4. **Bayport** (North Florida) — the SAS source treats this as ONE property with internal North/South building sub-sections. The approved spreadsheet instead lists it as TWO separate properties with two different addresses ("Cortland Bayport North" — 10150 Parkers Landing Dr, and "Cortland Bayport South" — 10510 Parkers Landing Dr, both Tampa FL). Display name intentionally NOT changed pending your decision: keep as one dropdown with one representative address, or split into two.
5. **Cortland at the Village** (Georgia) — the approved spreadsheet's address field reads "Lake Park Gate**" rather than a normal street address; the double-asterisk suggests a footnote that isn't visible in the data I can read. This property's name is confirmed and already applied, but its address is incomplete/unclear and should not be used for a map pin until clarified.
6. **Sugarland** (HASA) — no match; almost certainly the same community as the confirmed "Sugar Land" (Richmond, TX) elsewhere in the same pod's source, but the two spellings are not assumed identical without your confirmation.
7. **Las Casas** (Arizona) — no matching entry anywhere in the approved spreadsheet, despite being named in the source's Community Type list (Las Casas 1–14).
8. **The Point at Stockbridge** (Georgia) and **Lake' Edge** (Ohio/Tennessee) — no matching entries found; both are passing mentions in general-section lists (Fraud Watch and the voucher-accepting list respectively), not existing property dropdowns.
9. **This spreadsheet's own internal groupings do not match the SAS pod structure exactly** — for example, several Virginia properties (Pentagon City, National Landing, Arlington, Rosslyn) are filed under the spreadsheet's "Ohio & Tennessee" tab, and Nashville/Chicago/Birmingham properties appear there too. This reconciliation searched every sheet for every name regardless of which tab it was "expected" on, but it means the spreadsheet's sheet-per-pod organization should not be relied on as a map of the SAS pod structure.

## What changed in the live interface this pass

- All 11 pods: pod numbers removed from every learner-facing surface (cards, hero, chrome title, search, announcements); replaced with the approved market name above. Number badges converted to purely decorative, `aria-hidden` circles.
- Old pod labels (e.g. "GA Pod 1", "Pod 12") and old property shorthand (e.g. "The Village") remain searchable as hidden aliases — confirmed via testing that both the old and new terms find the right result, while only the approved name is ever displayed.
- 22 property display names applied across 8 pods, wherever the spreadsheet gave a single, unambiguous match (full list in Part 2 above).
- Nothing in Part 2 marked "NOT VERIFIED" or flagged above was changed — those properties still display their original SAS source wording.
- No address or coordinate data has been wired into any UI yet — that begins only once you've reviewed this table, per your required order of work.
