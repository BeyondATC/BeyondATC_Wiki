---
hide:
  - navigation
  - toc

og_image: https://wiki.beyondatc.net/assets/cards/card-cpdlc.png
og_description: Learn how to use CPDLC with BeyondATC's experimental feature for Pre-Departure Clearance (PDC).
description: Learn how to use CPDLC with BeyondATC's experimental feature for Pre-Departure Clearance (PDC).
---

# How to use CPDLC with BeyondATC

This guide shows you how to use CPDLC (Controller-Pilot Data Link Communications) with BeyondATC.  
Currently, only **Pre-Departure Clearance (PDC)** is supported and available **on the experimental branch**.

!!! info
    **Important:** CPDLC is in early development and only available in the **experimental branch** of BeyondATC. Only **PDC (Pre-Departure Clearance)** is functional in this version. Station login and pilot requests are **not yet supported**.

---

## What is CPDLC?

**Controller-Pilot Data Link Communications (CPDLC)** is a system that allows pilots and controllers to communicate via **text messages** instead of voice. This helps reduce frequency congestion and avoids miscommunication. CPDLC is already widely used in real-world aviation, especially for:

- **Clearances**: Routing, altitude, speed instructions
- **Requests**: Altitude changes, directs, etc.
- **Pre-Departure Clearance (PDC)**: IFR clearance before departure without using voice comms

---

## How CPDLC Works in BeyondATC

BeyondATC will implement CPDLC in **three stages**:

| Version | Features |
|--------|----------|
| **V1** | ✅ PDC (Pre-Departure Clearance) only *(available now)* |
| **V2** | 🔜 Station login + instructions via CPDLC |
| **V3** | 🔜 Pilot requests (altitude, directs, etc.) via CPDLC |

This guide focuses on **V1 – PDC**.

---

## ✅ Using PDC with BeyondATC

PDC allows you to get your IFR clearance via data link before pushback, instead of over the radio. With BeyondATC, this process works at **any airport**, regardless of real-world coverage at the moment.

### ✈️ Step-by-Step Setup

#### 1. **Make sure you’re using the experimental branch**

- Open BeyondATC
- Look at the bottom-left corner. If it says **EA**, go to your account tab and **enable Experimental Branch**.

#### 2. **Create your flight plan**

- Generate your flight as usual via **Simbrief**.

#### 3. **Connect to BeyondATC**

- Launch BeyondATC and connect as you normally would.

#### 4. **Enable BeyondATC CPDLC in your aircraft**

In your aircraft’s **ACARS settings**, choose **BeyondATC** as the CPDLC/ACARS provider.

**Supported aircraft (as of now):**

- Fenix Simulations A319 / A320 / A321

#### 5. **Set up your aircraft’s FMC/MCDU**

Before sending the PDC request:

- Your flight plan should be **loaded into the FMS/MCDU**
- Make sure your **callsign** and **route** match your Simbrief flight

#### 6. **Submit the PDC Request**

In your aircraft’s CPDLC interface:

- Go to the **PDC Request** page
- Fill in:
    - **Gate number**
    - **ATIS ID** (e.g., "D", from ATIS info Delta)
    - **Station** (ICAO code of departure airport, e.g., KJFK)
- Send the request

Then:

- Wait for the **ATC response** (it may take a few seconds)
- Once you receive your clearance, **read it carefully**
- Send back **WILCO** to acknowledge
- ATC will confirm you're **IFR cleared** – you're now ready to push and start!

---

## Specific tutorials by aircraft

### Fenix Simulation

<iframe width="560" height="315" src="https://www.youtube.com/embed/boZbAfJdq6A?si=UO3cmrDQ5HdDUFjg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
*Video made by our Community Mentor jason_91*

---

## 🔧 Developer Integration

Aircraft developers who want to support BeyondATC’s CPDLC system can contact us at:  
📧 **support@beyondatc.net**

We aim to keep integration simple and offer direct support to developers.

---

## 🐞 Feedback & Bugs

CPDLC is still in **active development**. Expect occasional bugs or limitations.  
To report issues or give feedback, visit our community thread:  
🔗 [CPDLC Feedback on Discord](https://discord.com/channels/1082413096045391915/1401551261266084010)
