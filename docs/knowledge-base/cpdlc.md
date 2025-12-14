---

og_image: https://wiki.beyondatc.net/assets/cards/card-cpdlc.png
og_description: Learn how to use CPDLC with BeyondATC.
description: Learn how to use CPDLC with BeyondATC.

---

# How to use CPDLC with BeyondATC

This page explains how CPDLC works in BeyondATC, what it can do, and what you need to know before using it.  

---

## What is CPDLC?

**CPDLC** is a digital communication system that allows pilots and ATC to exchange messages via **text** rather than voice.  
It is used heavily in modern aviation to:

- Reduce radio congestion  
- Improve clarity and reduce misunderstandings  
- Provide an efficient alternative to voice in busy or high-workload environments  

CPDLC is commonly used for:

- **Pre-Departure Clearances (PDC)**  
- **DCL (Data Link Departure Clearance)**  
- **Altitude, route, and speed instructions**  
- **Pilot requests** (directs, altitude changes, etc.)  
- **Information services** via ACARS (D-ATIS, METAR, etc.)

> **CPDLC supplements voice communication — it does not replace it.**

---

## What CPDLC/ACARS Can Do in BeyondATC

<div class="grid cards" markdown>

-   :material-airplane-takeoff:{ .lg .middle } __Pre-Departure Clearance (PDC) / DCL__

    ---

    Receive your IFR clearance via text before pushback, instead of calling clearance delivery.


-   :material-login:{ .lg .middle } __Controller Logon__

    ---

    Log on to Center controllers using a **logon code** shown in the BeyondATC **Frequencies** menu. Once logged on, appropriate instructions may be delivered via text.

-   :material-airplane:{ .lg .middle } __In-Flight Digital Requests__

    ---

    Send CPDLC messages such as:

    - Altitude change requests  
    - Direct-to waypoint requests  
    - Speed change requests  

    ATC replies using CPDLC when appropriate.

-   :material-weather-cloudy-clock:{ .lg .middle } __ACARS Weather & Information__

    ---

    Receive:

    - **D-ATIS**  
    - **METAR**

</div>

---

## Important Notes and Limitations

### Aircraft Must Support BeyondATC CPDLC  
BeyondATC’s CPDLC/ACARS system requires **aircraft developers** to implement support.  
It is **not** plug-and-play.

**Supported aircraft:**

- Fenix A319 / A320 / A321  
- iniBuilds A340 / A350  
- Fly the Maddog X MD-82 / MD-83 / MD-88  

If your aircraft does not list BeyondATC as a CPDLC/ACARS provider, CPDLC will **not work**.

Aircraft developers can contact:  
📧 **support@beyondatc.net**

### ACARS Weather support is Early-Stage  
Developers need time to add support for D-ATIS and METAR retrieval via BeyondATC’s ACARS system. Please wait until the aircraft developers have released the update to take advantage of this new feature.

---

## General Setup Flow (applies to all aircraft)

Each aircraft has its own menus, but the overall process is the same:

### 1. Select BeyondATC as CPDLC/ACARS Provider  
In your aircraft’s ACARS or CPDLC settings, choose **BeyondATC**. This setting is either in the aircraft external app or in the EFB/aircraft system

### 2. Load your flight plan  
Load your flight plan into both BeyondATC and your aircraft’s FMS/MCDU. Make sure all information in the FMS/MCDU is correct according to your flight plan (callsign and route).

### 3. Request PDC  
Find the PDC / Departure request page in your aircraft system and fill in the following information

- Gate number
- ATIS ID (you should listen to ATIS before requesting clearance)
- Station (ICAO code of the departure airport, e.g. KJFK)

You will then be able to send the request and receive your clearance. Acknowledge it by sending back WILCO. ATC will confirm your departure clearance.

!!! info  
    Messages through CPDLC/ACARS take a few seconds to be received.

### 4. Logon to center
Once you have departed, you will be able to logon to a center ATC.

- Identify the correct logon code for your FIR by checking the frequencies tab in BeyondATC. The logon code is available just below the center frequency.
- Open the ATC menu and find the connection/notification page
- Enter the center's logon code and notify
- ATC will then confirm by accepting the logon

Future instructions may arrive via text from now on.

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

Aircraft developers can integrate BeyondATC’s CPDLC/ACARS features using our official documentation.  
Support is available at:

📧 **support@beyondatc.net**

---

## Aircraft-Specific Tutorials

Here are the dedicated tutorials available:

- [Fenix A320 Family](cpdlc-a320fenix.md)
- iniBuilds A350 (work-in-progress)

!!! info  
    More tutorials and details are coming as this is currently a work-in-progress. Thank you for your patience.