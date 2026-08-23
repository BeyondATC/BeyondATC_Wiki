---
title: "VFR"
description: "The complete guide to VFR in BeyondATC: what is supported, how the three regions differ, and where to start for US, UK, and Australian flying."
og_description: "The complete guide to VFR in BeyondATC: what is supported, how the three regions differ, and where to start for US, UK, and Australian flying."
---

# VFR in BeyondATC

!!! warning "Experimental feature"
    VFR is in active development currently on the experimental branch, available in the Supporters Edition of BeyondATC; it is not fully complete. VFR will come to all customers as a free update once Stage Three is complete. Stage Two is our biggest update to VFR and adds dynamic airports, flight following, radar services, airspace transits, uncontrolled fields, aerodrome services, and COM2 support. As with any experimental release, you may encounter bugs or instability. AI VFR traffic, Special VFR and Vectoring within controlled airspace are not yet included.

VFR (Visual Flight Rules) in BeyondATC lets you fly under visual flight rules alongside IFR traffic with full ATC interaction, including the ability to do pattern work, get flight following, and land and take off at any airfield. BeyondATC models real-world procedures for three regions: the **United States**, the **United Kingdom**, and **Australia**.

While a flight plan is still needed, a VFR flight is not bound to it like an IFR flight. You can leave your departure field, pick up radar services, cross controlled airspace, land at an uncontrolled field, and continue, talking to each controller along the way, with airports loading dynamically around you.

---

## VFR Stages

VFR is being built in three stages. BeyondATC is currently on **Stage Two**, released on the experimental branch; VFR comes to all customers once Stage Three is complete.

<div class="vfr-stages" markdown>

| Feature | Stage One | Stage Two | Stage Three |
|---|:---:|:---:|:---:|
| Status | Complete | Current | Planned |
| **Regions** | US / UK / AUS | US / UK / AUS | US / UK / AUS |
| **Circuits** | :material-checkbox-marked:{ .vfr-done } | :material-checkbox-marked:{ .vfr-done } | :material-checkbox-marked:{ .vfr-done } |
| **Uncontrolled Fields** | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-marked:{ .vfr-done } | :material-checkbox-marked:{ .vfr-done } |
| **Airspace Rule Awareness** | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-marked:{ .vfr-done } | :material-checkbox-marked:{ .vfr-done } |
| **Zone Transits** | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-marked:{ .vfr-done } | :material-checkbox-marked:{ .vfr-done } |
| **Enroute Flight Following / Services** | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-marked:{ .vfr-done } | :material-checkbox-marked:{ .vfr-done } |
| **Different Controllers (AFIS/AGCS/FSS/LARS)** | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-marked:{ .vfr-done } | :material-checkbox-marked:{ .vfr-done } |
| **VFR Traffic** | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-marked:{ .vfr-done } |
| **SVFR** | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-marked:{ .vfr-done } |
| **VFR Vectoring and Deconfliction Instructions** | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-blank-outline:{ .vfr-blank } | :material-checkbox-marked:{ .vfr-done } |

</div>

---

## Supported regions

Procedures and phraseology differ by country. Each regional guide covers a complete flight from startup to arrival using that region's calls:

- 🇺🇸 **[United States](united-states.md)**: Class B/C/D airspace, Flight Following, Closed Traffic, Clearance Delivery
- 🇬🇧 **[United Kingdom](united-kingdom.md)**: Control Zones and VRPs, Basic and Traffic Services, Overhead joins, AFIS fields
- 🇦🇺 **[Australia](australia.md)**: Airways clearances, Surveillance Information Service, AWIS

We also have topic pages that apply no matter where you are flying: [Setting Up Your Flight](setting-up.md), [Uncontrolled Fields & Aerodrome Services](uncontrolled-fields.md), [Radios & COM2](radios.md), [Circuit Holds, Go-Arounds & Changes](sequencing-and-holds.md), [Callsigns & Squawks](callsigns-and-squawks.md), and the [Quick Reference](quick-reference.md).

---

## What's Currently Supported in VFR

**At the airport:**

- VFR departures from controlled or uncontrolled fields
- Circuit/pattern work with sequencing
- VFR arrivals with the ability to join the circuit or land at any airport
- Touch-and-go, full stop, low approach, stop and go (US/AU)
- Separation with IFR traffic in and around airports (go-arounds, orbit holds, extend downwind) with more in-depth vectoring and sequencing planned
- VFR Intersection departures
- Dynamic circuit intentions, runway, or circuit direction mid-flight
- Traffic alerting when in controlled airspace/flight following/traffic service

**In the wider world:**

- **Dynamic airports**: fly anywhere; controllers load around you, tune, talk, transit, land, and take off all in one flight
- **Flight following & radar services**: US flight following, UK Basic and Traffic Services (including LARS units), Australian surveillance information services
- **Airspace awareness**: US Class Bravo/Charlie/Delta classified from real airspace data, departure clearances at B/C fields, transition requests
- **Control zone transits**: cross a CTR with a clearance, routed via Visual Reference Points in the UK
- **Uncontrolled fields**: CTAF/UNICOM self-announcement frequencies with the ability to make blind calls (currently player only; AI VFR traffic arrives in Stage Three)
- **Aerodrome services**: AFIS/FISO ("Information"), Air/Ground radio, and US Flight Service Stations
- **COM2**: monitor any frequency on your second radio
- **Broadcast stations**: [AWOS, ASOS, and AWIS](../knowledge-base/atis/#asos-awos-awis-and-awib) weather frequencies

**General:**

- Regional phraseology and logic for US, UK, and Australia
- Flight plan import, MSFS world map, .pln, .lnmpln (Little NavMap), or SimBrief
- Callsign shortening for GA aircraft (region specific), similar-callsign detection
- Region-correct squawk assignment
- Sub-menu action buttons for faster interaction, and chained requests so you can make several requests in one call
- An airframe name library of over 880 aircraft types for traffic alert callouts

!!! info "Note"
    **AI VFR traffic is not yet supported.** AI VFR aircraft, VFR vectoring, and dynamic deconfliction between VFR aircraft are planned, releasing incrementally starting with enroute traffic.

---

## Regional Differences at a Glance

BeyondATC automatically detects the region from the airport's location and applies the correct phraseology. Here is a summary of the key differences you'll encounter:

| Feature | 🇺🇸 United States (FAA) | 🇬🇧 United Kingdom (CAP 413) | 🇦🇺 Australia (AIP) |
|---|---|---|---|
| **Startup** | Not required, contact Ground directly | Optional ("startup approved"; QNH comes later) | Optional ("start approved" + QNH) |
| **Pre-taxi clearance** | Required at Class B/C fields (Clearance Delivery) | None | Airways clearance at Class C |
| **Intentions wording** | "Closed traffic" / "traffic pattern" | "Circuits" | "Circuits" |
| **Squawk** | 1200 / discrete code at B/C or with flight following | Discrete code with the taxi or departure clearance (none at ATZ-only fields); "squawk conspicuity" when released or changing frequency | 3000 controlled / 1200 uncontrolled; discrete with services |
| **Pressure reference** | Altimeter (in. Hg) | QNH (hPa) | QNH (hPa) |
| **Circuit report point** | Midfield downwind | Downwind | Downwind |
| **Landing clearance given** | At downwind report (direct clearance) | On final | On base turn |
| **Radar service** | Flight following | Basic Service / Traffic Service | Surveillance Information Service |
| **Straight-in approach** | ✅ Available | ✅ Available | ✅ Available |
| **Stop and Go** | ✅ Available | ❌ | ✅ Available |
| **"The Option"** | ✅ Available | ❌ | ❌ |
| **Overhead join** | ❌ | ✅ Available | ❌ |

