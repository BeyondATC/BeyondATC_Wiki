---
title: "VFR | United Kingdom"
description: "A complete VFR flight in the United Kingdom with BeyondATC: startup and QNH, circuits, the overhead join, control zone entry via VRPs, Basic and Traffic Services, and zone transits."
og_description: "A complete VFR flight in the United Kingdom with BeyondATC: startup and QNH, circuits, the overhead join, control zone entry via VRPs, Basic and Traffic Services, and zone transits."
---

# 🇬🇧 VFR in the United Kingdom

The flow below covers a complete VFR flight from startup to arrival in the United Kingdom under CAP 413 phraseology, followed by zone transits, flight services, and join procedures. Ensure you have set up your flight plan first: [Setting Up Your Flight](setting-up.md).

---

## Startup

!!! info "Where to start"
    We recommend you spawn at a GA ramp or parking stand.

Optional: Contact Ground (or Delivery) to request startup **before** calling for taxi. ATC approves the startup; in the UK the QNH normally comes later, with your departure or join clearance (at fields without an ATIS it is included in the startup approval).

| Speaker                       | Response                                                                    |
| ----------------------------- | --------------------------------------------------------------------------- |
| :material-airplane: G-ABCD    | Bristol Ground, G-ABCD, Cessna 172 at Ramp 3, request startup for circuits. |
| :simple-tower: Bristol Ground | G-ABCD, Bristol Ground, startup approved.                                    |

---

## Request Taxi

Contact Ground and state your **intentions**: circuits or a VFR departure. BeyondATC requires you to include your intentions in the startup or taxi request. If you don't, ATC will ask you to clarify before issuing taxi instructions.

| Speaker                    | Response                                               |
| -------------------------- | ------------------------------------------------------ |
| :material-airplane: G-ABCD | Oxford Ground, G-ABCD, Piper PA-28, taxi for circuits. |

ATC will respond with runway and taxi routing. Follow the assigned route to the hold-short point. BeyondATC will hand you off to Tower when you reach the hold-short point.

!!! tip "Button users"
    Clicking "Request Taxi" will expand into a sub-menu where you can select your intention (circuits or departure) before transmitting.

---

## Intersection Departure (Optional)

If your aircraft's performance allows it, you can request to enter the runway at an intermediate taxiway intersection rather than taxiing to the full threshold.

**Two ways to request:**

1. **Action button**: The "Request Intersection Departure" button appears in the interface when valid intersections are available. Tap it to see the available options with remaining runway distance in feet.

2. **Voice during taxi**: Include the intersection in your taxi request:
   *"Request taxi, can accept Hotel."* or *"Request intersection Alpha."*

ATC will confirm the intersection and remaining runway available. In the UK the intersection is included in your taxi instructions.

!!! info "Note"
    Only intersections that leave enough runway for your aircraft's performance are offered. A Cessna 172 will see many options; a heavier aircraft may see few or none.

---

## Contact Tower & Request Departure

When you reach the hold-short point, either wait for BeyondATC to transfer you or switch to Tower yourself.

Report ready for departure with your runway; Tower already knows your intention from the taxi call.

| Speaker                    | Response                                                        |
| -------------------------- | --------------------------------------------------------------- |
| :material-airplane: G-ABCD | G-ABCD, ready for departure, runway 27.                         |

ATC evaluates the runway state and will issue one of the following:

| Instruction | Meaning |
|---|---|
| **Hold short** | Traffic on or approaching the runway |
| **Line up and wait** | Enter the runway but hold for takeoff clearance |
| **Cleared for takeoff** | All clear, takeoff clearance issued |

---

## Takeoff & Leaving the Area

When it is safe to do so, ATC will issue takeoff clearance.

| Speaker                     | Response                                                                   |
| --------------------------- | -------------------------------------------------------------------------- |
| :simple-tower: Oxford Tower | G-ABCD, Oxford Tower, wind 270 degrees 10 knots, runway 27, cleared for takeoff. |

If you are departing the area (not doing circuits), ensure you have requested a VFR departure. What happens next depends on airspace around the field.

| Field | What happens |
|---|---|
| **Control zone, Tower only** | Your zone clearance is issued with your departure clearance at the holding point: *"G-ABCD, hold position. Runway 27, after departure you are cleared to leave the Bristol control zone to the north, not above altitude 2,000 feet VFR, QNH 1013, squawk 4571."* Once airborne and clear, use **Report Leaving Control Zone** (or **Request Frequency Change**) and Tower releases you: *"G-ABCD, squawk conspicuity, freecall Cardiff Radar 119.155."* |
| **Control zone with its own Approach** | Tower transfers you to Approach at the ATZ boundary and Approach works you out through the zone under a radar control service (see below). |
| **ATZ only, or delegated under a neighbouring zone** | No zone clearance, as there is no zone to leave. A delegated field gives you a route and a cap instead: *"after departure route via the Redhill VRP, remaining outside the Gatwick control zone, not above altitude 1,400 feet."* Report leaving the ATZ and change frequency at your discretion. |

### Leaving controlled airspace with Approach

At a field with a separate Approach frequency, Tower hands you over as you leave the ATZ. Your zone clearance came from Tower on the ground, so Approach only needs your airborne call. Use **Announce On Frequency** or call by voice; until you do, Approach stays silent and no other actions are offered:

| Speaker                      | Response                                                                               |
| ---------------------------- | -------------------------------------------------------------------------------------- |
| :material-airplane: G-ABCD   | Bristol Radar, G-ABCD, airborne, climbing not above altitude 2,000 feet.               |
| :simple-tower: Bristol Radar | G-ABCD, Bristol Radar, identified, radar control service, report at the zone boundary. |
| :material-airplane: G-ABCD   | Wilco, report at the zone boundary, G-ABCD.                                     |

The boundary report instruction is only given when ATC cannot see the crossing on radar; otherwise the reply ends at *"radar control service"* and you answer *"roger"*. A **Report at Zone Boundary** button is available either way.

A few miles before the edge of controlled airspace, Approach asks what service you want outside it:

| Speaker                      | Response                                                                     |
| ---------------------------- | ---------------------------------------------------------------------------- |
| :simple-tower: Bristol Radar | G-ABCD, in 4 miles you will leave controlled airspace, what service do you require? |
| :material-airplane: G-ABCD   | Request Traffic Service, G-ABCD.                                             |

Answer with the **Basic Service**, **Traffic Service**, or **No Service**. When you cross the boundary, Approach confirms the service:

| Speaker                      | Response                                                               |
| ---------------------------- | ---------------------------------------------------------------------- |
| :simple-tower: Bristol Radar | G-ABCD, leaving controlled airspace, Traffic Service, report changing frequency. |
| :material-airplane: G-ABCD   | Traffic Service, wilco, G-ABCD.                                        |

If you decline a service, you are released instead:

| Speaker                      | Response                                                                        |
| ---------------------------- | ------------------------------------------------------------------------------- |
| :simple-tower: Bristol Radar | G-ABCD, leaving controlled airspace, squawk conspicuity, QNH 1013, frequency change approved. |


Approach keeps providing the service until you reach the edge of its radar coverage, then tells you:

| Speaker                      | Response                                                                                          |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| :simple-tower: Bristol Radar | G-ABCD, leaving my radar coverage, Traffic Service terminated, squawk conspicuity, suggest you freecall Cardiff Radar on 119.155. |

If no other unit is in range, the release ends with *"frequency change approved"* instead of a suggested station. From here you can call a LARS unit or London Information for a service of your own; see [Basic & Traffic Services](#basic-traffic-services).

!!! info "Note"
    If you do not answer the service question before the boundary, a Basic Service is assumed. While you are still inside the zone you are under a radar control service, so the Basic and Traffic Service request buttons only appear once you are outside controlled airspace.

### Returning to the field

If you're on a local flight and want to come back before you've left the area, you do not need to leave the zone and call again from outside. While you're still under your departure clearance, a **Return to Field** button is available on Tower. ATC answers with a join straight away:

| Speaker                         | Response                                                               |
| ------------------------------- | ---------------------------------------------------------------------- |
| :material-airplane: G-ABCD      | Ronaldsway Tower, G-ABCD, request rejoin.                              |
| :simple-tower: Ronaldsway Tower | G-ABCD, join right hand downwind, runway 26, not above altitude 1,000 feet VFR, QNH 1019, report downwind. |

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

You must report at the designated point for your region; in the UK this is **downwind**. At this point you also declare your **landing intention**.

**Landing intentions:**

| Option | Description |
|---|---|
| **Touch-and-go** | Land and immediately take off again |
| **Full stop** | Land and taxi to parking |
| **Low approach** | Fly low along the runway without landing |

| Speaker                    | Response                                                        |
| -------------------------- | --------------------------------------------------------------- |
| :material-airplane: G-ABCD | Oxford Tower, G-ABCD, downwind runway 27, request low approach. |

ATC responds with your sequence position. When you are number one you are told to report final; behind traffic you are told who to follow and to continue downwind:

| Speaker                     | Response                                         |
| --------------------------- | ------------------------------------------------ |
| :simple-tower: Oxford Tower | G-ABCD, roger, report final runway 27, number one. |

!!! tip "Changing your intention"
    After reporting, you can change your landing intention before clearance by using the "Change Intention" button or asking by voice. ATC will acknowledge and re-issue clearance with the updated intention.

!!! tip "Report Traffic In Sight"
    When sequenced behind traffic, ATC may ask you to report when you have the traffic in sight. A **Traffic In Sight** button will appear; you can also report it by voice.

---

## Continuing in the Circuit

If your intention is a touch-and-go or low approach, you stay in the circuit after each pass. Fly the circuit again and report downwind with your intention each time. Tower keeps sequencing you against other traffic until you leave in one of two ways:

| Leaving the circuit | How |
|---|---|
| **Full stop** | Report *"full stop"* at downwind. After landing, report clear of the runway and the [After Landing](#after-landing) flow takes over. |
| **Leaving the zone** | At a control zone airport, use the **Request To Leave The Control Zone** button, or ask by voice. ATC issues a zone exit clearance with any altitude restriction and a conspicuity squawk. |

By voice, say the whole thing in one call:

| Speaker                    | Response                                                                                           |
| -------------------------- | -------------------------------------------------------------------------------------------------- |
| :material-airplane: G-ABCD | Bristol Tower, G-ABCD, request to leave the Bristol control zone.                                  |
| :simple-tower: Bristol Tower | G-ABCD, cleared to leave the Bristol control zone, not above altitude 2,000 feet VFR, squawk conspicuity. |

At a field without controlled airspace there is no departure clearance to obtain. Use **Report Leaving The ATZ**, which opens a picker of the units you might want to call next, or say it by voice; ATC replies with a freecall to that unit:

| Speaker                     | Response                                                          |
| --------------------------- | ----------------------------------------------------------------- |
| :material-airplane: G-ABCD  | G-ABCD, leaving the ATZ to the north, request frequency change.   |
| :simple-tower: Oxford Tower | G-ABCD, freecall Brize Radar 124.280.                             |


!!! info "Note"
    If you want to depart the circuit make the request on the crosswind or downwind leg, so Tower can fit it in before issuing your next circuit clearance.

---

## Landing Clearance

Report final as you turn onto the final leg. ATC issues clearance on final.

| Speaker                     | Response                                                       |
| --------------------------- | -------------------------------------------------------------- |
| :material-airplane: G-ABCD  | Oxford Tower, G-ABCD, final runway 27.                         |
| :simple-tower: Oxford Tower | G-ABCD, surface wind 270 degrees, 10 knots, runway 27, cleared to land. |

!!! info "Note"
    **If the runway is occupied** when you report final, ATC defers your clearance until the runway is clear. You can request a go-around at any time during this phase.

    | Speaker                     | Response                       |
    | --------------------------- | ------------------------------ |
    | :simple-tower: Oxford Tower | G-ABCD, Oxford Tower, continue. |

---

## After Landing

Once you have landed and slowed, Tower tells you to vacate. At fields with a Ground frequency you are handed to Ground automatically once you are clear of the runway; at Tower-only fields Tower waits for your report.

| Speaker                     | Response                             |
| --------------------------- | ------------------------------------ |
| :simple-tower: Oxford Tower | G-ABCD, exit next available taxiway. |

Once you're off the runway, **Report Clear of Runway** either by button, which opens a sub-menu picker for your intention, or via voice. At a Tower-only field your report and request go out as **one call**:

| Intention | What happens |
|---|---|
| **Clear: Taxi to Parking** | ATC asks where you want to go: *"G-ABCD, roger, say preferred parking."* Pick a ramp from the buttons, choose **Any Ramp** for auto-assignment to the nearest suitable GA parking, or name it by voice. Taxi instructions follow. Naming the ramp in your clear-of-runway call skips the question. |
| **Clear: Circuits** | You are taxied back to the runway for more circuits. |
| **Clear: VFR Departure** | You are taxied back to the runway for departure from the area. |

| Speaker                     | Response                                                 |
| --------------------------- | -------------------------------------------------------- |
| :material-airplane: G-ABCD  | G-ABCD, clear of runway 27, request taxi to parking.     |
| :simple-tower: Oxford Tower | G-ABCD, roger, say preferred parking.                    |
| :material-airplane: G-ABCD  | Request North Apron, G-ABCD.                             |
| :simple-tower: Oxford Tower | G-ABCD, taxi to North Apron via Alpha.                   |

At fields with a separate Ground frequency, your clear-of-runway report is answered with a handoff. Read back the frequency and give Ground your intention there (**Taxi to Parking**, **Circuits**, or **VFR Departure**):

| Speaker                     | Response                             |
| --------------------------- | ------------------------------------ |
| :simple-tower: Oxford Tower | G-ABCD, roger, contact ground 121.9. |
| :material-airplane: G-ABCD  | Ground 121.9, G-ABCD.                |

If you report clear by voice without saying where you're headed, ATC asks: *"G-ABCD, roger, say intentions."*

---

## Arriving from Outside the Airport

If you are flying inbound and want to join the circuit, call Tower with **Request Join**. Tower replies with a squawk, the QNH and the runway in use, and asks for your message. Use **Pass Message** (or say it by voice) to give your aircraft type, route, position, altitude and intention:

| Speaker                     | Response                                                                                                              |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| :material-airplane: G-ABCD  | Oxford Tower, G-ABCD, request join.                                                                                   |
| :simple-tower: Oxford Tower | G-ABCD, Oxford Tower, squawk 7010, QNH 1013, runway 27 in use, pass your message.                                    |
| :material-airplane: G-ABCD  | PA-28 from Kemble to Oxford, 8 miles to the north of Oxford, altitude 2,000 feet on QNH 1013, VFR, inbound for landing, G-ABCD. |
| :simple-tower: Oxford Tower | G-ABCD, join left hand downwind, runway 27, not above altitude 1,000 feet VFR, QNH 1013, report downwind.            |

Three join types are available. ATC will issue one based on traffic and conditions:

| Join type | What happens |
|---|---|
| **Downwind join** | Join the downwind leg at circuit altitude |
| **Overhead join** | Full overhead procedure (see [The Overhead Join](#the-overhead-join) below) |
| **Straight-in** | Fly directly to final; report when established |

### Joining through a control zone

At fields with a separate **Approach** frequency, make the join request to Approach. The clearance adds the control zone entry, routed via a **Visual Reference Point**: you can pick a VRP from the **Request Join** sub-menu, name it in your transmission, or leave it out and ATC will pick the best one for you:

| Speaker                      | Response                                                                                                                          |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| :material-airplane: G-ABCD   | Bristol Radar, G-ABCD, request join.                                                                                              |
| :simple-tower: Bristol Radar | G-ABCD, Bristol Radar, squawk 7010, QNH 1013, runway 27 in use, pass your message.                                                |
| :material-airplane: G-ABCD   | PA-28 from Kemble to Bristol, 12 miles to the north of Bristol, altitude 2,000 feet on QNH 1013, VFR, inbound for landing, request join via Cheddar, G-ABCD. |
| :simple-tower: Bristol Radar | G-ABCD, cleared to enter the Bristol control zone VFR, route via Cheddar, join left hand downwind, runway 27, not above altitude 1,000 feet VFR, QNH 1013, report downwind. |

Report the entry point with **Report Overhead Cheddar**. Inside the zone you are under a radar control service; Approach transfers you to Tower once you report the aerodrome in sight:

| Speaker                      | Response                                                          |
| ---------------------------- | ----------------------------------------------------------------- |
| :material-airplane: G-ABCD   | G-ABCD, overhead Cheddar.                                         |
| :simple-tower: Bristol Radar | G-ABCD, roger, overhead Cheddar, radar control service, report aerodrome in sight. |
| :material-airplane: G-ABCD   | Aerodrome in sight, G-ABCD.                                       |
| :simple-tower: Bristol Radar | G-ABCD, contact Bristol Tower 133.850.                            |
| :material-airplane: G-ABCD   | Bristol Tower 133.850, G-ABCD.                                    |

Check in with Tower using **Announce On Frequency** and continue as normal from [Circuit Reporting](#circuit-reporting).

---

## The Overhead Join

The overhead join is a UK-specific procedure where you cross the airfield 1,000 ft above circuit altitude before descending to join downwind on the non-traffic (dead) side.

**Full sequence** (action buttons guide you through each step):

| Speaker                     | Response                                                                  |
| --------------------------- | ------------------------------------------------------------------------- |
| :simple-tower: Oxford Tower | G-ABCD, join overhead runway 27, altitude 2,200 feet VFR, QNH 1005, report overhead. |
| :material-airplane: G-ABCD  | G-ABCD, overhead.                                                         |
| :simple-tower: Oxford Tower | G-ABCD, report descending deadside.                                       |
| :material-airplane: G-ABCD  | G-ABCD, descending deadside.                                              |
| :simple-tower: Oxford Tower | G-ABCD, join left hand downwind, runway 27, report downwind.              |

You are now in the standard circuit; proceed as normal from [Circuit Reporting](#circuit-reporting).

---

## Basic & Traffic Services

Outside controlled airspace you can get a **Basic Service** (information only) or a **Traffic Service** (radar-derived traffic information), from LARS units (e.g. Brize Radar, Farnborough Radar), approach units, and London/Scottish Information.

To ask for a service, call up the relevant unit and ask for the service you require, ATC will ask you to pass your message, where you will pass your location, aircraft type, altitude and intentions:

| Speaker                    | Response                                                                                             |
| -------------------------- | ---------------------------------------------------------------------------------------------------- |
| :material-airplane: G-ABCD | Brize Radar, G-ABCD, request traffic service.                                                        |
| :simple-tower: Brize Radar | G-ABCD, Brize Radar, pass your message.                                                              |
| :material-airplane: G-ABCD | G-ABCD, PA-28 from Kemble to Exeter, 10 miles south of Kemble, altitude 3,000 feet on QNH 1013, VFR. |
| :simple-tower: Brize Radar | G-ABCD, squawk 3702.                                                                                 |
| :material-airplane: G-ABCD | Squawk 3702, G-ABCD.                                                                                 |
| :simple-tower: Brize Radar | G-ABCD, identified 10 miles south of Kemble, Traffic Service, Cotswold 1013.                         |

A Basic Service needs no identification, so it is granted in one step. Note, the pressure ("Cotswold 1013") Regional Pressure Setting, this gives you the QNH in the area you are flying in:

| Speaker                    | Response                                     |
| -------------------------- | -------------------------------------------- |
| :simple-tower: Brize Radar | G-ABCD, Basic Service, squawk 3702, Cotswold 1013. |


You can change between Basic and Traffic Service at any time with **Request Service**, cancel with *"service no longer required"*, and announce your departure from the frequency with **Report Changing Frequencies**.

---

## Zone Transits

Crossing UK Class D airspace requires a clearance, usually routed via **Visual Reference Points**. To request a transit, tune to the Approach frequency of the relevant airport and either use the **Request Zone Transit** button or ask for a zone transit verbally. You can ask for a service in the same call: *"request traffic service and zone transit"*.

### Requesting the transit

Approach answers with your squawk and asks for your message:

| Speaker                      | Response                                                                                                                                              |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| :material-airplane: G-ABCD   | Bristol Radar, G-ABCD, request zone transit.                                                                                                          |
| :simple-tower: Bristol Radar | G-ABCD, Bristol Radar, squawk 3702, pass your message.                                                                                                |
| :material-airplane: G-ABCD   | G-ABCD, PA-28 from Kemble to Exeter, 5 miles northeast of Bristol, altitude 2,500 feet on QNH 1013, VFR. Request transit via Cheddar and Chew Valley. |

The **Pass Message** button opens a sub menu to allow you to provide routing context:

| Option | What happens |
|---|---|
| **Routing: ATC Decides** | Your message asks for a transit and ATC picks the entry and exit points for you. |
| **Entry: {VRP}, then Exit: {VRP}** | Choose your own entry point, then your exit point. To ask ATC for specific entry and exit points. |

Of course you can name the points yourself over voice, like the example above, or leave them out and ATC decides the best route based on where you going.

!!! note "Changing VRP's"
    You can change your entry and exit VRP if you wish. The entry VRP can be changed up until you are in the Control Zone and the exit until you leave the control zone.

### The clearance

Once you are squawking correctly, Approach will identify you and clear you in to the zone. Currently transits always route via the active runway threshold. See an example clearance below:

| Speaker                      | Response                                                                                                                                                                                        |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| :simple-tower: Bristol Radar | G-ABCD, identified 5 miles northeast of Bristol, cleared to enter the Bristol control zone, routing via Cheddar, runway 27 threshold and Chew Valley, VFR, not above altitude 2,000 feet, Bristol QNH 1013, report entering the zone at Cheddar. |
| :material-airplane: G-ABCD   | Cleared to enter the Bristol control zone, routing via Cheddar, runway 27 threshold and Chew Valley, VFR, not above altitude 2,000 feet, QNH 1013, wilco, G-ABCD.                               |

The *"report entering the zone at …"* instruction is not always given; an identified aircraft is watched on radar, so ATC sometimes ends the clearance at the QNH. The report buttons are available either way.

### Standby, refusals and cancelling

ATC does not always clear you straight away:

| Situation | What ATC says |
|---|---|
| **Frequency busy** | *"G-ABCD, remain outside controlled airspace, I'll call you back."* Stay outside the zone; the clearance follows when the controller is free. |
| **Zone too busy** | *"G-ABCD, unable zone transit at this time due to controller workload, remain outside the Bristol control zone."* Nothing is latched; you can request again later. |
| **Called too early** | *"G-ABCD, you're still 18 miles from my airspace, call me back when you're closer."* |

!!! info "Changed your mind?"
    You can cancel before the clearance with **Cancel Transit Request**; ATC replies *"roger, transit request cancelled"* and you can ask again later.

### Entering the zone

Report your entry point with **Report Entering at {VRP}**. Inside the zone you are under a radar control service and receive traffic information:

| Speaker                      | Response                                                         |
| ---------------------------- | ---------------------------------------------------------------- |
| :material-airplane: G-ABCD   | G-ABCD, entering the zone at Cheddar.                            |
| :simple-tower: Bristol Radar | G-ABCD, roger, radar control service, report leaving the zone at Chew Valley. |

If you cross the boundary without reporting, ATC will still let you know:

| Speaker                      | Response                                                                         |
| ---------------------------- | -------------------------------------------------------------------------------- |
| :simple-tower: Bristol Radar | G-ABCD, entering controlled airspace, radar control service, report leaving the zone at Chew Valley. |


You can change your routing mid-transit: use **Change Entry VRP** before you enter the zone, or **Change Exit VRP** once you're inside, and ATC re-clears you via the new point:

| Speaker                      | Response                                                    |
| ---------------------------- | ----------------------------------------------------------- |
| :material-airplane: G-ABCD   | G-ABCD, can we enter by Cheddar?                            |
| :simple-tower: Bristol Radar | G-ABCD, roger, enter the Bristol control zone via the Cheddar VRP. |


### Crossing the ATZ

As you approach the aerodrome, Approach hands you to Tower for the runway crossing. Check in with Tower via **Announce On Frequency**:

| Speaker                      | Response                                                                          |
| ---------------------------- | --------------------------------------------------------------------------------- |
| :simple-tower: Bristol Radar | G-ABCD, contact Bristol Tower 133.850 for your crossing.                           |
| :material-airplane: G-ABCD   | Bristol Tower, G-ABCD, zone transit.                                              |
| :simple-tower: Bristol Tower | G-ABCD, Bristol Tower, cleared to route via the runway 27 threshold.               |
| :material-airplane: G-ABCD   | Route via the runway 27 threshold, G-ABCD.                                        |

Tower passes any relevant traffic before the instruction: *"traffic is a Cessna 172, 4 mile final"* or *"traffic is a Boeing 737, just departed"*. You should make your crossing at circuit height over the landing threshold. There may be times an arrival on short final conflicts with your crossing, in which case they take priority and Tower will hold you in an orbit and releases you once the runway is clear:

| Speaker                      | Response                                                                                     |
| ---------------------------- | -------------------------------------------------------------------------------------------- |
| :simple-tower: Bristol Tower | G-ABCD, Bristol Tower, traffic is an Airbus A320, 3 mile final. Orbit left, I'll call you back for crossing. |
| :material-airplane: G-ABCD   | Orbiting left, G-ABCD.                                                                       |
| :simple-tower: Bristol Tower | G-ABCD, continue crossing, route via the runway 27 threshold.                                |
| :material-airplane: G-ABCD   | Route via the runway 27 threshold, G-ABCD.                                                   |

Once you are across, Tower sends you back to Approach. Read back the frequency, then check in on the Approach frequency with **Announce On Frequency**:

| Speaker                      | Response                                                  |
| ---------------------------- | --------------------------------------------------------- |
| :simple-tower: Bristol Tower | G-ABCD, crossing complete, contact Bristol Radar 125.650. |
| :material-airplane: G-ABCD   | Bristol Radar 125.650, G-ABCD.                            |
| :material-airplane: G-ABCD   | Bristol Radar, G-ABCD, crossing complete.                 |
| :simple-tower: Bristol Radar | G-ABCD, radar control service, report overhead Chew Valley. |
| :material-airplane: G-ABCD   | Wilco, G-ABCD.                                            |

### Leaving the zone

Report your exit point with **Report Clear of Zone** (or **Report {VRP}**), or by voice. The radar control service ends at the boundary and the service you had before the zone is restored; if you had none, you leave with a Basic Service:

| Speaker                      | Response                                                  |
| ---------------------------- | --------------------------------------------------------- |
| :material-airplane: G-ABCD   | G-ABCD, overhead Chew Valley.                             |
| :simple-tower: Bristol Radar | G-ABCD, roger, leaving controlled airspace, Basic Service. |

If you leave without reporting, ATC will let you know:

| Speaker                      | Response                                                                              |
| ---------------------------- | ------------------------------------------------------------------------------------- |
| :simple-tower: Bristol Radar | G-ABCD, approaching the edge of controlled airspace, leaving controlled airspace, Basic Service. |

From here you will be under a basic service until you cancel it or leave Approaches area of responsibility. You can use **Report Changing Frequencies** to request a frequency change. See [Basic & Traffic Services](#basic-traffic-services).

---

## See also

- [Uncontrolled Fields & Aerodrome Services](uncontrolled-fields.md)
- [Radios & COM2](radios.md)
- [Circuit Holds, Go-Arounds & Changes](sequencing-and-holds.md)
- [Callsigns & Squawks](callsigns-and-squawks.md)
- [Quick Reference](quick-reference.md)
