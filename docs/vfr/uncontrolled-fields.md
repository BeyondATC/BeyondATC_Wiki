---
title: "VFR | Uncontrolled Fields & Aerodrome Services"
description: "Self-announcing on CTAF/UNICOM at fields with no ATC, and the information-only stations in between: AFIS/FISO, Air/Ground radio, and Flight Service Stations."
og_description: "Self-announcing on CTAF/UNICOM at fields with no ATC, and the information-only stations in between: AFIS/FISO, Air/Ground radio, and Flight Service Stations."
---

# Uncontrolled Fields & Aerodrome Services

## Uncontrolled Fields: CTAF & UNICOM

!!! warning "CTAF & UNICOM Traffic"
    Stage Two does not have AI VFR traffic, this will come with Stage Three - as such CTAF and UNICOM frequencies will have no other traffic communicating on them

Unlike controlled airspace, at fields with no ATC, you will usually broadcast your intentions **in the blind**. Tune the CTAF/UNICOM and the interface switches to announce buttons covering the whole visit:

| Phase | Announcements |
|---|---|
| Ground | Taxi (departure / circuits / parking), backtrack, lining up |
| Departure | Departing north/east/south/west, or remaining in the pattern |
| Inbound | Inbound, overflying |
| Circuit | Crosswind (🇬🇧🇦🇺), downwind, base, final (downwind, base and final with your intention) |
| UK joins | Joining overhead, descending dead side |
| Going around | Going around (while airborne) |
| After landing | Clear of runway |

An example broadcast:

| Speaker                    | Response                                                                                   |
| -------------------------- | ------------------------------------------------------------------------------------------ |
| :material-airplane: N123AB | Half Moon Bay traffic, N123AB, entering left downwind runway 30, full stop, Half Moon Bay. |

!!! info "Note"
    Regional wording is applied depending on where you fly.

---

## Broadcast Frequencies

Most untowered fields carry their own CTAF or UNICOM frequency from the airport's data; tune it and the announce buttons appear. On top of that, BeyondATC recognizes some well-known broadcast frequencies:

| Frequency | Name | Mainly Used In |
|---|---|---|
| 122.700, 122.725, 122.800, 122.950, 122.975, 123.000, 123.050, 123.075 | UNICOM | United States |
| 122.900, 122.925 | MULTICOM | United States |
| 126.700 | MULTICOM | Australia |
| 135.480 (also 135.475) | SAFETYCOM | United Kingdom |
| 121.500 | GUARD (Monitor only) | Worldwide |

!!! info "Note"
    These frequencies are broadcast only - meaning no one will reply to your broadcasts. We plan to have VFR Traffic make their own announcements on these frequencies when Stage Three is released.

---

## Aerodrome Services: Information, Radio & FSS

Some fields have a different controller or service station rather than a fully functional control tower. Each is modelled with the limits on what the operator may say:

| Station | What it can do |
|---|---|
| **AFIS / FISO** (🇬🇧 "{Field} Information") | Taxi and traffic **information** and reports, but it has no legal right to issue clearances. Expect wording like *"take off at your discretion."* |
| **Air/Ground radio** (🇬🇧 AGCS) | Information only. Your taxi call becomes *"request taxi **information**"*. |
| **Flight Service Stations** (🇺🇸) | Airfield information, weather, and PIREPs. |

!!! note "Combined Requests"
    Certain requests support 'combined requests', for example *"request airfield information and taxi for VFR departure."*
