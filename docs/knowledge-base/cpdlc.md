---
og_image: https://wiki.beyondatc.net/assets/cards/card-cpdlc.png
og_description: Learn how to use CPDLC with BeyondATC.
description: Learn how to use CPDLC with BeyondATC.
---

# How to use CPDLC/ACARS with BeyondATC

This page explains how CPDLC / ACARS works in BeyondATC, what it can do, and what you need to know before using it.

---

## What is CPDLC/ACARS?

CPDLC (Controller–Pilot Data Link Communications) is a digital communication system that allows ATC and pilots to exchange operational ATC messages via text instead of voice.

It is used in modern aviation to:

- Reduce radio congestion
- Improve clarity and reduce misunderstandings
- Support operations in busy or high-workload environments

CPDLC is used for ATC communications, including:

- Altitude, route, and speed instructions
- Frequency changes
- Pilot requests (directs, climbs/descents, etc.)

!!! note ""
    **CPDLC supplements voice communication — it does not replace it.**

ACARS (Aircraft Communications Addressing and Reporting System) is a data transmission system used to send and receive digital messages between aircraft and ground systems.

ACARS acts as a transport layer and is used for a wide range of services, including:

- Pre-Departure Clearances (PDC / DCL)
- Information services (D-ATIS, METAR)

---

## What CPDLC/ACARS Can Do in BeyondATC

<div class="grid cards" markdown>

-   :material-airplane-takeoff:{ .lg .middle } **Pre-Departure Clearance (PDC) / DCL**

    ---

    Receive your IFR clearance via text before pushback, instead of calling clearance delivery.

-   :material-login:{ .lg .middle } **Controller Logon**

    ---

    Log on to Center controllers using a **logon code** shown in the BeyondATC **Frequencies** menu. Once logged on, appropriate instructions may be delivered via text.

-   :material-airplane:{ .lg .middle } **In-Flight Digital Requests**

    ---

    Send CPDLC messages such as:

    - Altitude change requests
    - Direct-to waypoint requests

    ATC replies using CPDLC when appropriate.

-   :material-cloud-sync-outline:{ .lg .middle } **ACARS Weather & Information**

    ---

    Receive:

    - **D-ATIS**
    - **METAR**

</div>

---

## Important Notes and Limitations

### Aircraft Must Support BeyondATC CPDLC/ACARS

BeyondATC's CPDLC/ACARS system requires **aircraft developers** to implement support.  
It is **not** plug-and-play.

**Supported aircraft:**

Natively supported:

- Fenix A319 / A320 / A321
- FlyByWire A320
- FSLabs A320 / A321
- iniBuilds A340 / A350
- Headwinds A330
- Fly the Maddog X MD-82 / MD-83 / MD-88

Supported with an additional addon:

- Asobo Citation Longitude ([Garmin 3000/5000 CPDLC and Simbrief](https://flightsim.to/file/98506/garmin-3000-5000-cpdlc-and-simbrief))
- Asobo Daher TBM9 ([Garmin 3000/5000 CPDLC and Simbrief](https://flightsim.to/file/98506/garmin-3000-5000-cpdlc-and-simbrief))
- Liv2Air Cj3+ ([Garmin 3000/5000 CPDLC and Simbrief](https://flightsim.to/file/98506/garmin-3000-5000-cpdlc-and-simbrief))
- Asobo Cirrus Vision Jet MSFS 2024 ([Garmin 3000/5000 CPDLC and Simbrief](https://flightsim.to/file/98506/garmin-3000-5000-cpdlc-and-simbrief))

*Please note that this list might not be exhaustive. Check your aircraft addon if BeyondATC is listed as a CPDLC/ACARS provider. Let us know if any addon is missing!*

If your aircraft does not list BeyondATC as a CPDLC/ACARS provider, CPDLC will **not work**.

Aircraft developers can contact us to get all information about integrating BeyondATC in their aircraft systems on this email address:  
📧 **support@beyondatc.net**

### ACARS Weather support is Early-Stage

Developers need time to add support for D-ATIS and METAR retrieval via BeyondATC's ACARS system. Please wait until the aircraft developers have released the update to take advantage of this new feature.

---

## General Setup Flow (applies to all aircraft)

Each aircraft has its own menus, but the overall process is the same:

### 1. Select BeyondATC as CPDLC/ACARS Provider

In your aircraft's ACARS or CPDLC settings, choose **BeyondATC**. This setting is either in the aircraft external app or in the EFB/aircraft system

### 2. Load your flight plan

Load your flight plan into both BeyondATC and your aircraft's FMS/MCDU. Make sure all information in the FMS/MCDU is correct according to your flight plan (callsign and route).

### 3. Request PDC

Find the PDC / Departure request page in your aircraft system and fill in the following information

- Gate number
- ATIS ID (you should listen to ATIS before requesting clearance)
- Station (ICAO code of the departure airport, e.g. KJFK)

You will then be able to send the request and receive your clearance. Acknowledge it by sending back WILCO. ATC will confirm your departure clearance.

!!! info
    Messages through CPDLC/ACARS can take up to 40 seconds for messages to be sent and received as this is not an instant system.

### 4. Logon to center

Once you have departed, you will be able to logon to a center ATC.

- Identify the correct logon code for your FIR by checking the frequencies tab in BeyondATC. The logon code is available just below the center frequency.
- Open the ATC menu and find the connection/notification page
- Enter the center's logon code and notify
- ATC will then confirm by accepting the logon

You'll start to see appropriate CPDLC instructions be sent over text instead of voice.

### 5. Receive, respond and make requests via CPDLC

#### Handoffs

You will receive handoffs instructions via CPDLC. Make sure to update the frequency and the logon code if you don't have auto-tune on. When joining a new frequency, you are expected to check in via voice (the instruction is CONTACT and not MONITOR).

#### Direct-to

You can request a direct-to via CPDLC. Find the request page in the ATC menu and fill the direct-to field with the wanted fix.

#### Altitude change

You can change your cruise altitude via CPDLC.

Aircraft-specific guides will show exact steps and menus. Find the request page in the ATC menu and fill the altitude you want to request.

---

## Developer Integration

Aircraft developers can integrate BeyondATC's CPDLC/ACARS by contacting us at:

📧 **support@beyondatc.net**

---

## Aircraft-Specific Tutorials

Here are the dedicated tutorials available:

- [Fenix A320 Family](cpdlc-a320fenix.md)
- iniBuilds A350 (work-in-progress)

!!! info
    More tutorials and details are coming as this is currently a work-in-progress. Thank you for your patience.