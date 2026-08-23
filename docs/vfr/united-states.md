---
title: "VFR | United States"
description: "A complete VFR flight in the United States with BeyondATC: Class B/C departure clearances, closed traffic, landing clearances, flight following and airspace transitions."
og_description: "A complete VFR flight in the United States with BeyondATC: Class B/C departure clearances, closed traffic, landing clearances, flight following and airspace transitions."
---

# 🇺🇸 VFR in the United States

The flow below covers a complete VFR flight from startup to arrival in the United States under FAA phraseology, followed by airspace and radar services. Ensure you have set up your flight plan first: [Setting Up Your Flight](setting-up.md).

!!! info "Flying in Canada?"
    When flying VFR in Canada, BeyondATC will use US rules.

---

## Startup
!!! info "Where to start"
    We recommend you spawn at a GA ramp or parking stand.

There is no separate startup step in the US. At a **Class D** field, contact **Ground** directly to request taxi; no startup button is offered.

At a **Class B or C** field, a pre-taxi departure clearance is required first, see the next step.

---

## Class B/C Departure Clearance

Departing a Class B or C airport requires a call to **Clearance Delivery** before taxi. Use **Request VFR Departure**, or add flight following with **VFR Departure + Flight Following**:

**Class C departure:**

| Speaker                          | Response                                                                          |
| -------------------------------- | --------------------------------------------------------------------------------- |
| :material-airplane: N123AB       | Burbank Clearance, N123AB, Cessna 172, with information Foxtrot, VFR to Van Nuys. |
| :simple-tower: Burbank Clearance | N123AB, maintain VFR at or below 3,000, departure frequency 124.6, squawk 5566.   |
| :material-airplane: N123AB       | VFR at or below 3,000, departure 124.6, squawk 5566, N123AB.                      |
| :simple-tower: Burbank Clearance | N123AB, readback correct. Contact ground 121.7 when ready to taxi.                |

**Class B departure** (the clearance and readback carry the airspace):

| Speaker                              | Response                                                                                                       |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| :material-airplane: N123AB           | Los Angeles Clearance, N123AB, Cessna 172, with information Bravo, VFR to Santa Monica.                        |
| :simple-tower: Los Angeles Clearance | N123AB, cleared out of the Los Angeles Bravo airspace, maintain VFR at or below 2,500, departure frequency 125.2, squawk 4521. |
| :material-airplane: N123AB           | Cleared out of the Los Angeles Bravo, VFR at or below 2,500, departure 125.2, squawk 4521, N123AB.             |
| :simple-tower: Los Angeles Clearance | N123AB, readback correct. Contact ground 121.65 when ready to taxi.                                            |

Closed traffic does not need a clearance: state it in your taxi call to Ground. If you ask Clearance Delivery for closed traffic, you will be redirected to Ground.

---

## Request Taxi

Contact Ground and state your **intentions**: pattern work or a VFR departure. BeyondATC requires you to include your intentions in the startup or taxi request. If you don't, ATC will ask you to clarify before issuing taxi instructions.

**Example (pattern work):**

| Speaker                    | Response                                                     |
| -------------------------- | ------------------------------------------------------------ |
| :material-airplane: N123AB | Burbank Ground, N123AB, Cessna 172, request taxi for closed traffic. |

**Example (departure):**

| Speaker                    | Response                                                    |
| -------------------------- | ----------------------------------------------------------- |
| :material-airplane: N123AB | Burbank Ground, N123AB, Cessna 172, request taxi for VFR departure. |

**Example (departure with flight following):**

| Speaker                    | Response                                                                                        |
| -------------------------- | ----------------------------------------------------------------------------------------------- |
| :material-airplane: N123AB | Burbank Ground, N123AB, Cessna 172, request taxi for VFR departure to the north, with flight following. |

ATC will respond with runway and taxi routing. If you asked for flight following, Ground first gives you the departure frequency and squawk, then the taxi instructions after your readback:

| Speaker              | Response                                          |
| -------------------- | ------------------------------------------------- |
| :simple-tower: Burbank Ground | N123AB, departure frequency 124.6, squawk 5566.  |
| :material-airplane: N123AB | Departure 124.6, squawk 5566, N123AB.       |

Follow the assigned route to the hold-short point. BeyondATC will hand you off to Tower when you reach the hold-short point.

!!! tip "Button users"
    Clicking "Request Taxi" will expand into a sub-menu: **Taxi: Closed Traffic**, **Taxi: Departure**, or **Taxi: Departure w/ Flight Following** (which then asks for a direction). Voice users can include their intention in the initial call to skip this step. If you already hold a Class B/C clearance, ATC knows your intention and a plain "Request Taxi" goes straight to taxi instructions.

---

## Intersection Departure (Optional)

If your aircraft's performance allows it, you can request to enter the runway at an intermediate taxiway intersection rather than taxiing to the full threshold.

**Two ways to request:**

1. **Action button**: The "Request Intersection Departure" button appears in the interface when valid intersections are available. Tap it to see the available options with remaining runway distance in feet.

2. **Voice during taxi**: Include the intersection in your taxi request:
   *"Request taxi, can accept Hotel."* or *"Request intersection Alpha."*

ATC confirms the intersection and remaining runway in the taxi instructions, and the takeoff clearance names it again:

| Speaker              | Response                                                                        |
| -------------------- | ------------------------------------------------------------------------------- |
| :simple-tower: Burbank Ground | N123AB, runway 27 at Alpha, taxi via Bravo. Intersection departure, 3,500 feet available. |
| :simple-tower: Burbank Tower | N123AB, runway 27 at Alpha, cleared for takeoff.                        |


!!! info "Note"
    Only intersections that leave enough runway for your aircraft's performance are offered. A Cessna 172 will see many options; a heavier aircraft may see few or none.

---

## Contact Tower & Request Departure

When you reach the hold-short point, either wait for BeyondATC to transfer you or switch to Tower yourself.

Report ready for departure with your runway; Tower already knows your intention from your taxi call.

| Speaker                    | Response                                 |
| -------------------------- | ---------------------------------------- |
| :material-airplane: N123AB | N123AB, ready for departure, runway 27.  |

ATC evaluates the runway state and will issue one of the following:

| Instruction | Meaning |
|---|---|
| **Hold short** | Traffic on or approaching the runway |
| **Line up and wait** | Enter the runway but hold for takeoff clearance |
| **Cleared for takeoff** | All clear, takeoff clearance issued |

---

## Takeoff & Leaving the Area

ATC will issue takeoff clearance with wind information. For pattern work, the traffic direction (left or right traffic) is included.

| Speaker              | Response                                                                   |
| -------------------- | -------------------------------------------------------------------------- |
| :simple-tower: Palo Alto Tower | N123AB, wind 270 at 10, runway 27, cleared for takeoff, make left traffic. |

If you are departing the area (not doing closed traffic):

| Airspace | What happens |
|---|---|
| **Class D** | You are automatically released from tower control when you leave the Class D. No frequency change request is needed, although you can request one if you wish. |
| **Class B/C** | Tower hands you to Departure once you are airborne and about half a mile from the field: *"contact Burbank Departure 124.6."* Check in with **Announce On Frequency** (*"Burbank Departure, N123AB, off Burbank, passing 1,500"*) and you will get *"radar contact"*, along with flight following if you asked for it. |

!!! tip "Requesting flight following after departure"
    You can ask for flight following in the air if you didn't ask for it on the ground, click the "Request Flight Following" button or ask by voice.

### Returning to the field

If you're on a local flight and want to come back before you've left the area, you do not need to leave the airspace and call again from outside. While you're still under your departure clearance, a **Return to Field** button is available on Tower. ATC answers with a pattern entry straight away:

| Speaker                       | Response                                                          |
| ----------------------------- | ----------------------------------------------------------------- |
| :material-airplane: N123AB    | Van Nuys Tower, N123AB, request return to the field.              |
| :simple-tower: Van Nuys Tower | N123AB, enter left downwind runway 16R, report midfield downwind. |

If you've already been handed to Departure, they'll send you back to Tower for the rejoin.

---

## Joining the Pattern

After takeoff, fly the pattern at the airport's pattern altitude. The standard pattern consists of five legs:

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

You must report at the designated point for your region; in the US this is **midfield downwind**. At this point you also declare your **landing intention**.

**Landing intentions:**

| Option | Description |
|---|---|
| **Touch-and-go** | Land and immediately take off again |
| **Full stop** | Land and taxi back to the runway or parking |
| **Low approach** | Fly low along the runway without landing |
| **Stop and go** | Land, come to a full stop on the runway, then take off again |
| **The option** | The landing intention is left to the pilot |

| Speaker                    | Response                                                  |
| -------------------------- | --------------------------------------------------------- |
| :material-airplane: N123AB | N123AB, downwind runway 27, touch and go.                 |

ATC responds with your sequence and, when no traffic is ahead, the landing clearance in the same call (see [Landing Clearance](#landing-clearance)). Behind other pattern traffic the sequence and clearance are combined:

| Speaker              | Response                                                                                     |
| -------------------- | -------------------------------------------------------------------------------------------- |
| :simple-tower: Palo Alto Tower | N123AB, number two, follow the Cessna 172 on downwind, wind 270 at 10, runway 27, cleared touch and go. |

!!! tip "Changing your intention"
    After reporting, you can change your landing intention before clearance by using the "Change Intention" button or asking by voice. ATC will acknowledge and re-issue clearance with the updated intention.

!!! tip "Report Traffic In Sight"
    When sequenced behind traffic, ATC may ask you to report when you have the traffic in sight. A **Traffic In Sight** button will appear; you can also report it by voice.

---

## Continuing in the Pattern

If your intention is a touch-and-go, low approach, stop-and-go, or the option, you stay in the pattern after each pass. Fly the circuit again and report midfield downwind with your intention each time. Tower keeps sequencing you against other traffic until you leave in one of two ways:

| Leaving the pattern | How |
|---|---|
| **Full stop** | Report *"full stop"* at midfield downwind. After landing, report clear of the runway and the [After a Full Stop Landing](#after-a-full-stop-landing) flow takes over. |
| **Request Departure** | Leave the pattern and the area. Use the **Request Departure** button, or **Request Departure w/ Flight Following** if you want radar services on the way out. Either button opens a direction picker (north, northeast, and so on, or no preference). |

By voice, say the whole thing in one call:

| Speaker                    | Response                                                                |
| -------------------------- | ----------------------------------------------------------------------- |
| :material-airplane: N123AB | N123AB, request departure to the north.                                 |
| :simple-tower: Palo Alto Tower | N123AB, departure to the north approved, frequency change approved. |

With flight following, ATC assigns a squawk and hands you to the radar facility instead:

| Speaker                    | Response                                                                            |
| -------------------------- | ----------------------------------------------------------------------------------- |
| :material-airplane: N123AB | N123AB, request departure to the north with flight following.                       |
| :simple-tower: Palo Alto Tower | N123AB, departure to the north approved, squawk 4521, contact SoCal Departure 124.6. |

While you hold a landing or touch-and-go clearance the departure buttons are hidden; complete the pass first, then ask on the climb-out or downwind. If no radar facility covers the field, the flight-following form is answered with the squawk only.

!!! info "Note"
    The automatic Class D release described under [Takeoff & Leaving the Area](#takeoff-leaving-the-area) applies to aircraft that took off as a VFR departure. If you are working the pattern, Tower expects a departure request before you leave, whatever the airspace class.

---

## Landing Clearance

In the US, if there is no traffic conflict, landing clearance is issued **at the downwind report**; there is no separate "report final" step. When you report midfield downwind with your intention, ATC responds directly:

| Situation | ATC response |
|---|---|
| **No traffic ahead** | Clearance is issued immediately with wind and intention: *"N123AB, wind 270 at 10, runway 27, cleared touch and go."* |
| **Traffic ahead** | You are sequenced: *"N123AB, number 2, follow the Cessna 172 on 2 mile final, report traffic in sight."* Once you report the traffic and it is safe to do so, ATC issues clearance. |

If you want a different intention after the clearance is issued, pick one of the alternative **Request: …** buttons shown in place of the readback (or say it) and ATC re-issues the clearance. Once the readback is complete the intention is locked for that pass.

| Speaker                    | Response                                  |
| -------------------------- | ----------------------------------------- |
| :material-airplane: N123AB | Request full stop, N123AB.                |
| :simple-tower: Palo Alto Tower | N123AB, roger, runway 27, cleared to land. |


!!! info "Note"
    When landing at an airfield, **If the runway is occupied** when you report final, ATC will defer your clearance until the runway is clear. In the pattern if you reach short final without a clearance, Tower will either clear you or send you around. You can also report a go-around at any time.

    | Speaker              | Response                  |
    | -------------------- | ------------------------- |
    | :simple-tower: Palo Alto Tower | N123AB, Palo Alto Tower, continue. |

---

## After a Full Stop Landing

Once you have landed and slowed, Tower tells you to vacate. At fields with a Ground frequency you are handed to Ground automatically once you are clear of the runway; at Tower-only fields Tower will wait for you to report your taxi intentions.

| Speaker              | Response                            |
| -------------------- | ----------------------------------- |
| :simple-tower: Palo Alto Tower | N123AB, exit next available taxiway. |


Once you're off the runway you can **Report Clear of Runway** either by button, which opens a sub-menu picker for your intention, or via voice.

| Intention | What happens |
|---|---|
| **Clear: Taxi to Parking** | ATC asks where you want to go: *"N123AB, roger, say preferred parking."* Pick a ramp from the buttons, choose **Any Ramp** for auto-assignment to the nearest suitable GA parking or say the parking name via voice. |
| **Clear: Closed Traffic** | You are taxied back to the active runway for more pattern work. |
| **Clear: VFR Departure** | You are taxied back to the active runway for departure from the area. |

| Speaker                        | Response                                                              |
| ------------------------------ | --------------------------------------------------------------------- |
| :material-airplane: N123AB     | N123AB, clear of runway 31, request taxi to parking.                  |
| :simple-tower: Palo Alto Tower | N123AB, roger, say preferred parking.                                 |
| :material-airplane: N123AB     | Request North Ramp, N123AB.                                           |
| :simple-tower: Palo Alto Tower | N123AB, taxi to North Ramp via Alpha.                                 |

At fields with a separate Ground frequency, your clear-of-runway report is answered with a handoff. Read back the frequency and give Ground your intention there (**Taxi to Parking**, **Closed Traffic**, or **VFR Departure**):

| Speaker                    | Response                          |
| -------------------------- | --------------------------------- |
| :simple-tower: Palo Alto Tower | N123AB, roger, contact ground 121.9. |
| :material-airplane: N123AB | Ground 121.9, N123AB.             |

If you report clear by voice without saying where you're headed, ATC will ask you for your intention.

---

## Arriving from Outside the Airport

If you are flying inbound, call up Tower with the **Report Inbound**. This will expands into **Inbound: Landing** or **Inbound: Pattern Work**. You will then provide your information using the **Position Report** button (type, distance, direction, altitude, intention and ATIS letter) and ATC answers with the pattern entry. By voice you can say the whole thing in one call:

| Speaker                          | Response                                                                                                     |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| :material-airplane: N123AB       | Palo Alto Tower, N123AB, Cessna 172, inbound for landing, with information Alpha.                            |
| :material-airplane: N123AB       | Palo Alto Tower, N123AB, Cessna 172, five miles to the west at 2,500 feet, inbound for landing, with information Alpha, N123AB. |
| :simple-tower: Palo Alto Tower   | N3AB, Palo Alto Tower, enter left downwind runway 27, report midfield downwind.                               |

Depending on where you are, ATC may instead give you a base entry or a straight-in:

| Speaker              | Response                                          |
| -------------------- | ------------------------------------------------- |
| :simple-tower: Palo Alto Tower | N123AB, enter left base runway 27, report final.  |
| :simple-tower: Palo Alto Tower | N123AB, make straight-in runway 27, report 3 mile final. |

If you would rather have one of the others, the **Request straight-in** / **Request base entry** buttons are offered with the clearance.

**Class B/C fields:** the inbound call belongs to **Approach**, not Tower. Call the approach frequency, get a squawk and (at Bravo) *"cleared into the Class Bravo airspace"*, and you'll be sequenced and handed to Tower at about 7 miles. If you call too early Tower they will redirect you back to approach.

---

## Flight Following

Flight following allows you to receive radar advisories from Approach or Center while flying VFR. There are three ways you can ask for flight following:

| When | How |
|---|---|
| **On the ground, with your taxi call** | *"…request taxi for VFR departure to the north, with flight following."* |
| **With your Class B/C departure clearance** | Use the **VFR Departure + Flight Following** button. |
| **In the air** | Call the overlying radar facility: *"SoCal Approach, N123AB, request flight following to Santa Monica."* |

After asking ATC for flight following they will want further information, use the **Pass Message** or give your type, route, position and altitude. ATC then assigns a squawk, radar-identifies you, and starts calling traffic to you:

| Speaker                       | Response                                                                          |
| ----------------------------- | --------------------------------------------------------------------------------- |
| :simple-tower: SoCal Approach | N123AB, SoCal Approach, go ahead.                                                 |
| :material-airplane: N123AB    | N123AB, Cessna 172, from Burbank to Santa Monica, 12 miles west of Van Nuys, altitude 4,500 feet, VFR. |
| :simple-tower: SoCal Approach | N123AB, squawk 4521 and ident.                                                    |
| :material-airplane: N123AB    | Squawk 4521 and ident, N123AB.                                                    |
| :simple-tower: SoCal Approach | N123AB, radar contact, 12 miles west of Van Nuys, altimeter 29.92.                |
| :simple-tower: SoCal Approach | N3AB, traffic two o'clock, three miles, opposite direction, 4,500.                |

Respond with **Traffic In Sight** (*"traffic in sight"*) or **Looking for Aircraft** (*"looking for traffic"*). You'll be handed between sectors as you fly. Check in on each new sector, and cancel any time with *"cancel flight following"*:

| Speaker                       | Response                                                          |
| ----------------------------- | ----------------------------------------------------------------- |
| :material-airplane: N3AB      | SoCal Approach, N3AB, level 5,500.                                |
| :material-airplane: N3AB      | N3AB, cancel flight following.                                    |
| :simple-tower: SoCal Approach | N3AB, radar service terminated, squawk 1200, frequency change approved. |


!!! tip "Flight following must be requested"
    Flight following is only provided when you request it using one of the methods above.

---

## Airspace Transitions

You may need to cross controlled airspace on your VFR flight. Request the transition from the controller that owns the airspace.

| Speaker                        | Response                                                                                                                      |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| :material-airplane: N738FE     | Nantucket Tower, N738FE, Cessna 208, 8 miles east of Nantucket Memorial at 3,000, request transition through the Class Delta. |
| :simple-tower: Nantucket Tower | N738FE, proceed through the Class Delta as requested, maintain VFR.                                                           |

The button label follows the airspace: **Request Bravo Transition**, **Request Charlie Transition**, or **Request Delta Transition**. What ATC says on entry and when you leave the airspace depends on the class:

| Airspace | Entry clearance | Release on exit |
|---|---|---|
| **Bravo** | *"N738FE, radar contact, 8 miles east of Nantucket Memorial, cleared through the Boston Bravo airspace, maintain VFR at or below 3,500."* | *"N738FE, leaving the Boston Bravo airspace, radar service terminated, squawk VFR, frequency change approved."* |
| **Charlie** | *"N738FE, transition through the Nantucket Charlie approved, maintain VFR."* | *"N738FE, clear of the Nantucket Charlie, radar service terminated, squawk VFR, frequency change approved."* |
| **Delta** | *"N738FE, proceed through the Class Delta as requested, maintain VFR."* | *"N738FE, clear of the Class Delta, frequency change approved."* |

!!! info "Flying below airspace"
    Remember, if you are flying below airspace you do not need a clearance.

---

## See also

- [Uncontrolled Fields & Aerodrome Services](uncontrolled-fields.md)
- [Radios & COM2](radios.md)
- [Circuit Holds, Go-Arounds & Changes](sequencing-and-holds.md)
- [Callsigns & Squawks](callsigns-and-squawks.md)
- [Quick Reference](quick-reference.md)
