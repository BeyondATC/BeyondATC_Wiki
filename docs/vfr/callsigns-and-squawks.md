---
title: "VFR | Callsigns & Squawks"
description: "How BeyondATC shortens GA callsigns by region, assigns region-correct squawk codes, handles similar callsigns, and models controller workload."
og_description: "How BeyondATC shortens GA callsigns by region, assigns region-correct squawk codes, handles similar callsigns, and models controller workload."
---

# Callsigns, Squawks & Controller Workload

## Callsign Shortening

To save time, BeyondATC will shorten GA callsigns after two way communication is established:

| Region | Full callsign | Shortened | Style |
|---|---|---|---|
| 🇺🇸 US | N42PC (Piper Comanche) | Piper 2PC | Type prefix + last 3 of N-number |
| 🇬🇧 UK | G-ABCD | G-CD | First letter + last 2 |
| 🇦🇺 AU | VH-BVM | BVM | Last 3 (VH prefix dropped) |

Your shortened callsign appears under the full form at the bottom right of the flight interface (**G-ABCD** with **(G-CD)** beneath it). You can use either form when transmitting.

## Squawks, Similar Callsigns & Workload

- **Region-correct squawk assignment**: We've mapped discrete codes depending on the region you are flying; so if you are mad enough to do a VFR atlantic crossing - a European conspicuity code won't follow you into the US.
- **Similar callsign detection**: when another aircraft on frequency sounds like you, ATC transmits a one-time advisory, *"caution, similar callsign on frequency, use full callsign"*, and both aircraft revert to full callsigns.
- **Controller workload**: on a busy frequency a join or zone transit request may receive *"standby"*; the controller calls you back when free.