---
title: "VFR | Australia"
description: "A complete VFR flight in Australia with BeyondATC: start approval and QNH, Class C airways clearances, circuits with base-turn clearances, Surveillance Information Service, and AWIS."
og_description: "A complete VFR flight in Australia with BeyondATC: start approval and QNH, Class C airways clearances, circuits with base-turn clearances, Surveillance Information Service, and AWIS."
---

# 🇦🇺 VFR in Australia

The flow below covers a complete VFR flight from startup to arrival in Australia under AIP phraseology, followed by the airways clearances and services specific to Australia. Ensure you have set up your flight plan first: [Setting Up Your Flight](setting-up.md).

!!! info "Flying in NZ?"
    When flying VFR in New Zealand, BeyondATC will use AUS rules.

---

## Startup

!!! info "Where to start"
    We recommend you spawn at a GA ramp or parking stand.

Optional: Contact Ground (or Delivery) to request start **before** calling for taxi. ATC will approve your startup and pass the airports QNH.

| Speaker                         | Response                                                                      |
| ------------------------------- | ----------------------------------------------------------------------------- |
| :material-airplane: VH-ABC      | Bankstown Ground, VH-ABC Piper Archer at Ramp 2, request startup for circuits. |
| :simple-tower: Bankstown Ground | VH-ABC, Bankstown Ground start approved, QNH 1019.                             |

---

## Airways Clearance (Class C)

Class C aerodromes require an **airways clearance** before taxi. Use **Request Airways Clearance** after startup:

| Speaker                             | Response                                                                              |
| ----------------------------------- | ------------------------------------------------------------------------------------- |
| :material-airplane: VH-ABC          | Gold Coast Delivery, VH-ABC, Piper Archer, VFR to Brisbane, received Bravo, request clearance. |
| :simple-tower: Gold Coast Delivery  | VH-ABC, cleared to Brisbane, not above 1,500 feet, departure frequency 125.6, squawk 3651. |
| :material-airplane: VH-ABC          | Cleared to Brisbane, not above 1,500 feet, departure 125.6, squawk 3651, VH-ABC.        |

!!! info "Class D Aerodromes"
    Class D aerodromes need no airways clearance.

---

## Request Taxi

Contact Ground and state your **intentions**: circuits or a VFR departure. BeyondATC requires you to include your intentions in the startup or taxi request. If you don't, ATC will ask you to clarify before issuing taxi instructions. If you already hold an airways clearance, ATC knows your intention and a plain "Request Taxi" goes straight to taxi instructions.

| Speaker                    | Response                                                           |
| -------------------------- | ------------------------------------------------------------------ |
| :material-airplane: VH-ABC | Bankstown Ground, VH-ABC, Piper Archer, request taxi for circuits. |

ATC will respond with runway and taxi routing. Follow the assigned route to the hold-short point. BeyondATC will hand you off to Tower when you reach the hold-short point.

!!! tip "Button users"
    Clicking "Request Taxi" will expand into a sub-menu where you can select your intention (circuits or departure) before transmitting. Voice users can state their intention in the initial call to skip this step.

---

## Intersection Departure (Optional)

If your aircraft's performance allows it, you can request to enter the runway at an intermediate taxiway intersection rather than taxiing to the full threshold.

**Two ways to request:**

1. **Action button**: The "Request Intersection Departure" button appears in the interface when valid intersections are available. Tap it to see the available options with remaining runway distance in feet.

2. **Voice during taxi**: Include the intersection in your taxi request:
   *"Request taxi, can accept Hotel."* or *"Request intersection Alpha."*

ATC will confirm the intersection and remaining runway available. In Australia the intersection is included in your taxi instructions.

!!! info "Note"
    Only intersections that leave enough runway for your aircraft's performance are offered. A Cessna 172 will see many options; a heavier aircraft may see few or none.

---

## Contact Tower & Request Departure

When you reach the hold-short point, either wait for BeyondATC to transfer you or switch to Tower yourself.

Report ready for departure with your runway; Tower already knows your intention from the taxi call. Tower answers with your circuit or departure instructions, a squawk, and a hold:

| Speaker                        | Response                                                                                                          |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------- |
| :material-airplane: VH-ABC     | VH-ABC, ready for departure, runway 29.                                                                           |
| :simple-tower: Bankstown Tower | VH-ABC, hold position. After departure runway 29, enter left circuit, not above 1,500 feet, squawk 3000.          |
| :material-airplane: VH-ABC     | Hold position. Runway 29, after departure left circuit, not above 1,500 feet, squawk 3000, VH-ABC.                |

For a departure the instruction is a zone clearance instead. At a Class C aerodrome your airways clearance already covers this:

| Speaker                        | Response                                                                                                   |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------- |
| :simple-tower: Bankstown Tower | VH-ABC, hold position. Runway 29, after departure you are cleared to leave the Bankstown control zone, not above 2,500 feet, squawk 3000. |
| :material-airplane: VH-ABC     | Hold position. Runway 29. After departure, cleared to leave the Bankstown control zone, not above 2,500 feet, squawk 3000, VH-ABC. |


ATC then evaluates the runway state and will issue one of the following:

| Instruction | Meaning |
|---|---|
| **Hold short** | Traffic on or approaching the runway |
| **Line up and wait** | Enter the runway but hold for takeoff clearance |
| **Cleared for takeoff** | All clear, takeoff clearance issued |

---

## Takeoff & Leaving the Area

When it is safe to do so, ATC will issue takeoff clearance. For circuits, the circuit direction is included.

| Speaker                        | Response                                                                                          |
| ------------------------------ | ------------------------------------------------------------------------------------------------- |
| :simple-tower: Bankstown Tower | VH-ABC, Bankstown Tower, wind 270 degrees 10 knots, runway 29, cleared for takeoff, left hand circuits. |

If you are departing the area (not doing circuits), what happens next depends on the aerodrome.

| Aerodrome | What happens |
|---|---|
| **Class D, Tower only** | Once airborne and clear of the circuit, use **Request Frequency Change** (or say *"clear of the zone"*). Tower releases you: *"VH-ABC, frequency change approved, squawk 1200."* |
| **Class C with its own Approach** | Tower transfers you to Approach once you are airborne and Approach works you out through the zone under a radar control service (see below). |

### Leaving controlled airspace with Approach

At a Class C aerodrome Tower hands you over shortly after takeoff. Your airways clearance already covers the zone, so Approach only needs your airborne call:

| Speaker                        | Response                              |
| ------------------------------ | ------------------------------------- |
| :simple-tower: Gold Coast Tower | VH-ABC, contact Gold Coast Approach 125.6. |
| :material-airplane: VH-ABC     | Gold Coast Approach 125.6, VH-ABC.      |

Use **Announce On Frequency** or call by voice; until you do, Approach stays silent and no other actions are offered:

| Speaker                         | Response                                                                                 |
| ------------------------------- | ---------------------------------------------------------------------------------------- |
| :material-airplane: VH-ABC      | Gold Coast Approach, VH-ABC, airborne, climbing not above altitude 1,500 feet.             |
| :simple-tower: Gold Coast Approach | VH-ABC, Gold Coast Approach, identified, radar control service, report at the zone boundary. |
| :material-airplane: VH-ABC      | Wilco, report at the zone boundary, VH-ABC.                                              |

The boundary report instruction is only given when ATC cannot see the crossing on radar; otherwise the reply ends at *"radar control service"* and you answer *"roger"*. A **Report at Zone Boundary** button is available either way.

At the edge of controlled airspace the radar service ends and you are released with the VFR squawk:

| Speaker                         | Response                                                                              |
| ------------------------------- | ------------------------------------------------------------------------------------- |
| :simple-tower: Gold Coast Approach | VH-ABC, leaving controlled airspace, surveillance service terminated, squawk 1200.     |
| :material-airplane: VH-ABC      | Squawk 1200, VH-ABC.                                                                  |

If you want radar services outside controlled airspace, ask Centre for flight following; see [Surveillance Information Service](#surveillance-information-service).

### Returning to the field

If you're on a local flight and want to come back before you've left the area, you do not need to leave the zone and call again from outside. While you're still under your departure clearance, a **Return to Field** button is available on Tower. ATC answers with a join straight away:

| Speaker                        | Response                                              |
| ------------------------------ | ----------------------------------------------------- |
| :material-airplane: VH-ABC     | Bankstown Tower, VH-ABC, request rejoin.              |
| :simple-tower: Bankstown Tower | VH-ABC, join left downwind, runway 29, not above altitude 1,500 feet, QNH 1019, report downwind. |

If you've already been handed to Approach, they'll send you back to Tower for the rejoin.

---

## Joining the Circuit

After takeoff, fly the circuit at the airport's circuit altitude. The standard circuit consists of five legs:

```
   <---------------------  [Downwind]  <---------------------
   |                                                         ^
   v                                                         |
[Base]                                                  [Crosswind]
   |                                                         ^
   v                                                         |
    --->  [Final]  --->  [== Runway ==]  --->  [Upwind]  --->
```

BeyondATC tracks your position within the circuit and sequences you against IFR traffic.

---

## Circuit Reporting

You must report at the designated point for your region; in Australia this is **downwind**, and ATC then asks you to report turning base. At this point you also declare your **landing intention**.

**Landing intentions:**

| Option | Description |
|---|---|
| **Touch-and-go** | Land and immediately take off again |
| **Full stop** | Land and taxi to parking |
| **Low approach** | Fly low along the runway without landing |
| **Stop and go** | Land, come to a full stop, then take off from the same runway |

| Speaker                    | Response                                                   |
| -------------------------- | ---------------------------------------------------------- |
| :material-airplane: VH-ABC | VH-ABC, downwind runway 29, touch and go.                  |

ATC responds with your sequence position and tells you to report turning base; when you are behind traffic you are told who to follow, depending on the situation you may be asked to orbit:

| Speaker                        | Response                                             |
| ------------------------------ | ---------------------------------------------------- |
| :simple-tower: Bankstown Tower | VH-ABC, number one, report turning base, runway 29.  |

!!! tip "Changing your intention"
    After reporting, you can change your landing intention before clearance by using the "Change Intention" button or asking by voice. ATC will acknowledge and re-issue clearance with the updated intention.

!!! tip "Report Traffic In Sight"
    When sequenced behind traffic, ATC may ask you to report when you have the traffic in sight. A **Traffic In Sight** button will appear; you can also report traffic in sight by voice.

---

## Continuing in the Circuit

If your intention is a touch-and-go, low approach, or stop-and-go, you stay in the circuit after each pass. Fly the circuit again and report downwind and base with your intention each time. Tower keeps sequencing you against other traffic until you leave in one of two ways:

| Leaving the circuit | How |
|---|---|
| **Full stop** | Report *"full stop"* at downwind. After landing, report clear of the runway and the [After Landing](#after-landing) flow takes over. |
| **Frequency change** | Use the **Request Frequency Change** button, or say *"request frequency change"* or *"clear of the zone"*. ATC approves the change and assigns the VFR squawk. |

By voice, say the whole thing in one call:

| Speaker                        | Response                                                     |
| ------------------------------ | ------------------------------------------------------------ |
| :material-airplane: VH-ABC     | Bankstown Tower, VH-ABC, request frequency change.           |
| :simple-tower: Bankstown Tower | VH-ABC, frequency change approved, squawk 1200.              |

Make the request on the crosswind or downwind leg, before your next downwind report, so Tower can fit it in before issuing your next clearance.

---

## Landing Clearance

You report your intentions at downwind and ATC will instruct you to report turning base. Clearance is then issued when you report turning base.

| Speaker                        | Response                                                            |
| ------------------------------ | ------------------------------------------------------------------- |
| :material-airplane: VH-ABC     | VH-ABC, turning base, runway 29.                                    |
| :simple-tower: Bankstown Tower | VH-ABC, wind 270 degrees 10 knots, runway 29, cleared touch and go. |

!!! info "Note"
    **If the runway is occupied** when you report turning base, ATC defers your clearance until the runway is clear. You can request a go-around at any time during this phase.

    | Speaker                        | Response                          |
    | ------------------------------ | --------------------------------- |
    | :simple-tower: Bankstown Tower | VH-ABC, Bankstown Tower, continue. |

---

## After Landing

Once you have landed and slowed, Tower tells you to vacate. At fields with a Ground frequency you are handed to Ground automatically once you are clear of the runway; at Tower-only fields Tower waits for your report.

| Speaker                        | Response                             |
| ------------------------------ | ------------------------------------ |
| :simple-tower: Bankstown Tower | VH-ABC, exit next available taxiway. |


Once you're off the runway you can **Report Clear of Runway** either by button, which opens a sub-menu picker for your intention, or via voice. Your report and request go out as **one call**:

| Intention | What happens |
|---|---|
| **Clear: Taxi to Parking** | ATC asks where you want to go: *"VH-ABC, roger, say preferred parking."* Pick a ramp from the buttons, choose **Any Ramp** for auto-assignment to the nearest suitable GA parking, or name it by voice. Taxi instructions follow. Naming the ramp in your clear-of-runway call skips the question. |
| **Clear: Circuits** | Your state is reset and you are taxied back for more circuits. |
| **Clear: VFR Departure** | You are taxied to the runway for a departure from the area. |

| Speaker                        | Response                                                 |
| ------------------------------ | -------------------------------------------------------- |
| :material-airplane: VH-ABC     | VH-ABC, clear of runway 29, request taxi to parking.     |
| :simple-tower: Bankstown Tower | VH-ABC, roger, say preferred parking.                    |
| :material-airplane: VH-ABC     | Request Ramp 2, VH-ABC.                                  |
| :simple-tower: Bankstown Tower | VH-ABC, taxi to Ramp 2 via Alpha.                        |

At fields with a separate Ground frequency, your clear-of-runway report is answered with a handoff. Read back the frequency and give Ground your intention there (**Taxi to Parking**, **Circuits**, or **VFR Departure**):

| Speaker                        | Response                            |
| ------------------------------ | ----------------------------------- |
| :simple-tower: Bankstown Tower | VH-ABC, roger, contact ground 119.9. |
| :material-airplane: VH-ABC     | Ground 119.9, VH-ABC.               |

If you report clear by voice without saying where you're headed, ATC asks: *"VH-ABC, roger, say intentions."*

---

## Arriving from Outside the Airport

If you are flying inbound and want to join the circuit, call Tower with **Request Join**. Tower replies with the runway in use and asks for your message. You'll need to pass your message (**Pass Message** action) and give your aircraft type, position, altitude and intention:

| Speaker                        | Response                                                                                                   |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| :material-airplane: VH-ABC     | Bankstown Tower, VH-ABC, request join.                                                                     |
| :simple-tower: Bankstown Tower | VH-ABC, Bankstown Tower, runway 29 in use, pass your message.                                              |
| :material-airplane: VH-ABC     | Piper Archer, 6 miles to the south-west of Bankstown, altitude 1,800 feet, inbound, VH-ABC.                |
| :simple-tower: Bankstown Tower | VH-ABC, join left downwind, runway 29, wind 270 degrees 10 knots, not above altitude 1,500 feet, QNH 1019, report downwind. |
| :material-airplane: VH-ABC     | Join left downwind, runway 29, not above altitude 1,500 feet, QNH 1019, wilco, VH-ABC.                    |

A straight-in approach may be offered instead when your position suits it:

| Speaker                        | Response                                              |
| ------------------------------ | ----------------------------------------------------- |
| :simple-tower: Bankstown Tower | VH-ABC, make straight-in approach, runway 29, report final. |


At **Class C** aerodromes the inbound call belongs to Approach. Call before the boundary with **Request Join**; Approach identifies you and issues an arrival clearance, and your *"field in sight"* report triggers the transfer to Tower:

| Speaker                          | Response                                                                                                     |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| :simple-tower: Gold Coast Approach  | VH-ABC, identified, cleared to Gold Coast, not above 1,500 feet, expect runway 14, QNH 1019. Report field in sight. |
| :material-airplane: VH-ABC       | Cleared to Gold Coast, not above 1,500 feet, runway 14, QNH 1019, VH-ABC.                                   |
| :material-airplane: VH-ABC       | Gold Coast Approach, VH-ABC, field in sight.                                                                |
| :simple-tower: Gold Coast Approach  | VH-ABC, contact Gold Coast Tower 118.7.                                                                  |

---

## Surveillance Information Service

The Australian equivalent of flight following, requested from Centre with **Request Flight Following**. Centre asks for your message, assigns a squawk, and identifies you:

| Speaker                          | Response                                                                                                 |
| -------------------------------- | -------------------------------------------------------------------------------------------------------- |
| :material-airplane: VH-ABC       | Melbourne Centre, VH-ABC, request flight following.                                                      |
| :simple-tower: Melbourne Centre  | VH-ABC, Melbourne Centre, pass your message.                                                             |
| :material-airplane: VH-ABC       | VH-ABC, Piper Archer, from Bankstown to Canberra, 20 miles south-west of Bankstown, altitude 4,500 feet, VFR. |
| :simple-tower: Melbourne Centre  | VH-ABC, squawk 3651.                                                                                     |
| :material-airplane: VH-ABC       | Squawk 3651, VH-ABC.                                                                                     |
| :simple-tower: Melbourne Centre  | VH-ABC, identified, 20 miles south-west of Bankstown.                                                    |

Centre will then monitor and call out relevant traffic to you. Where you can respond with **Traffic In Sight** or **Looking for Aircraft**. You are handed between sectors as you fly, and to your destination Approach if it's at a Class C aerodrome. Cancel this enroute service at any time with *"terminate surveillance service."*

!!! info "AWIS"
    Australia also has **[AWIS](../knowledge-base/atis/#asos-awos-awis-and-awib)**, automated aerodrome weather stations, which provide aerodrome weather information for smaller fields

---

## Zone Transits

Crossing Class C airspace requires a clearance. Tune to the relevant Approach frequency of the relevant aerodrome and use **Request Zone Transit**, or ask by voice. You can ask for flight following in the same call.

### Requesting the transit

Approach answers with your squawk and invites your message:

| Speaker                          | Response                                                                                                                      |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| :material-airplane: VH-ABC       | Gold Coast Approach, VH-ABC, request zone transit.                                                                           |
| :simple-tower: Gold Coast Approach  | VH-ABC, Gold Coast Approach, squawk 3651, pass your message.                                                              |
| :material-airplane: VH-ABC       | VH-ABC, Piper Archer, from Bankstown to Brisbane, 10 miles south of Gold Coast, altitude 2,500 feet on QNH 1019, VFR.       |

Where the aerodrome has **visual reporting points**, the **Pass Message** button opens a routing picker first: **Routing: ATC Decides**, or **Entry: {point}** then **Exit: {point}**. If you are using voice you can name the points yourself or leave them out and ATC will decide the best route.

### The clearance

Once you are squawking, Approach will identify you and clears you into controlled airspace. Transits route via the active runway threshold:

| Speaker                          | Response                                                                                                                                                        |
| -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| :simple-tower: Gold Coast Approach  | VH-ABC, identified 10 miles south of Gold Coast, cleared to enter the Gold Coast control zone, via the runway 14 threshold, VFR, not above altitude 1,500 feet, QNH 1019, report clear of the zone. |
| :material-airplane: VH-ABC       | Cleared to enter the Gold Coast control zone, via the runway 14 threshold, VFR, not above altitude 1,500 feet, QNH 1019, wilco, VH-ABC.                       |

!!! info "Note"
    The *"report …"* instruction is not always given; an identified aircraft is watched on radar, so ATC sometimes ends the clearance at the QNH. The report buttons are available either way.

### Standby, refusals and cancelling

ATC does not always clear you straight away, depending on airspace traffic and controller workload:

| Situation | What ATC says |
|---|---|
| **Frequency busy** | *"VH-ABC, remain outside controlled airspace, I'll call you back."* Stay outside the zone; the clearance follows when the controller is free. |
| **Zone too busy** | *"VH-ABC, unable zone transit at this time due to controller workload, remain outside the Gold Coast control zone."* Nothing is latched; you can request again later. |
| **Called too early** | *"VH-ABC, you're still 18 miles from my airspace, call me back when you're closer."* |

!!! info "Changed your mind?"
    You can cancel before the clearance with **Cancel Transit Request**; ATC replies *"roger, transit request cancelled"* and you can ask again later, here or at another zone.

### Entering the zone

When you cross the boundary, ATC confirms the service. Inside the zone you are under a radar control service and receive traffic information:

| Speaker                          | Response                                                         |
| -------------------------------- | ---------------------------------------------------------------- |
| :simple-tower: Gold Coast Approach  | VH-ABC, entering controlled airspace, radar control service.  |
| :material-airplane: VH-ABC       | Radar control service, VH-ABC.                                   |

### Crossing the runway

As you approach the aerodrome, Approach hands you to Tower for the runway crossing. Check in with **Announce On Frequency**:

| Speaker                          | Response                                                                |
| -------------------------------- | ----------------------------------------------------------------------- |
| :simple-tower: Gold Coast Approach  | VH-ABC, contact Gold Coast Tower 118.7 for your crossing.           |
| :material-airplane: VH-ABC       | Gold Coast Tower 118.7, VH-ABC.                                        |
| :material-airplane: VH-ABC       | Gold Coast Tower, VH-ABC, zone transit.                                |
| :simple-tower: Gold Coast Tower  | VH-ABC, Gold Coast Tower, cleared to route via the runway 14 threshold. |
| :material-airplane: VH-ABC       | Route via the runway 14 threshold, VH-ABC.                              |

Tower passes any relevant traffic before the instruction: *"traffic is a Cessna 172, 4 mile final"*. Make your crossing at circuit height over the landing threshold. Arrivals takes priority over crossing aircraft so Tower may hold you in an orbit and release you once the runway is clear:

| Speaker                          | Response                                                                                           |
| -------------------------------- | -------------------------------------------------------------------------------------------------- |
| :simple-tower: Gold Coast Tower  | VH-ABC, Gold Coast Tower, traffic is a Boeing 737, 3 mile final. Orbit left, I'll call your crossing. |
| :material-airplane: VH-ABC       | Orbiting left, VH-ABC.                                                                             |
| :simple-tower: Gold Coast Tower  | VH-ABC, continue crossing, route via the runway 14 threshold.                                      |
| :material-airplane: VH-ABC       | Route via the runway 14 threshold, VH-ABC.                                                         |

Once you are across, Tower sends you back to Approach. Read back the frequency, then check back in with Approach via **Announce On Frequency**:

| Speaker                          | Response                                                        |
| -------------------------------- | --------------------------------------------------------------- |
| :simple-tower: Gold Coast Tower  | VH-ABC, crossing complete, contact Gold Coast Approach 125.6.  |
| :material-airplane: VH-ABC       | Gold Coast Approach 125.6, VH-ABC.                             |
| :material-airplane: VH-ABC       | Gold Coast Approach, VH-ABC, crossing complete.                |
| :simple-tower: Gold Coast Approach | VH-ABC, radar control service, report clear of the zone.     |
| :material-airplane: VH-ABC       | Wilco, VH-ABC.                                                 |

### Leaving the zone

Report clear with **Report Clear of Zone**, or by voice. The radar control service ends at the boundary; if you had flight following before the zone it is restored, otherwise you continue with flight following from the same unit:

| Speaker                          | Response                                                          |
| -------------------------------- | ----------------------------------------------------------------- |
| :material-airplane: VH-ABC       | VH-ABC, clear of the zone.                                        |
| :simple-tower: Gold Coast Approach  | VH-ABC, roger, leaving controlled airspace, Flight Following.  |

From here the normal service rules apply: keep it, cancel with *"terminate surveillance service"*, or change frequency.

---

## See also

- [Uncontrolled Fields & Aerodrome Services](uncontrolled-fields.md)
- [Radios & COM2](radios.md)
- [Circuit Holds, Go-Arounds & Changes](sequencing-and-holds.md)
- [Callsigns & Squawks](callsigns-and-squawks.md)
- [Quick Reference](quick-reference.md)
