---
title: "VFR | Circuit Holds, Go-Arounds & Changes"
description: "How BeyondATC sequences VFR circuit traffic against IFR arrivals: extend downwind, orbits, breakouts, go-arounds, and changing your runway or circuit direction."
og_description: "How BeyondATC sequences VFR circuit traffic against IFR arrivals: extend downwind, orbits, breakouts, go-arounds, and changing your runway or circuit direction."
---

# Circuit Holds, Go-Arounds & Changes

## Traffic Sequencing & Circuit Holds

!!! warning "Work In Progress"
    VFR Sequencing is a work in progress, it is not a complete system and expects the player to maintain separation with traffic at all times, even in controlled airspace.

BeyondATC integrates VFR circuit traffic with inbound IFR traffic. When an IFR aircraft is on approach, ATC may issue a hold instruction to keep you clear.

### Extend Downwind

Used for lighter IFR conflicts when you are on the downwind leg.

| Region | Instruction |
|---|---|
| 🇺🇸 US | *"Extend your downwind, I'll call your base."* |
| 🇬🇧 UK | *"Continue downwind."* or *"Extend downwind, I'll call your base."* |
| 🇦🇺 AU | *"Extend downwind, I'll call your base."* |

ATC will call you back when it's safe to turn base:

| Region | Callback |
|---|---|
| 🇺🇸 US | *"Turn base."* |
| 🇬🇧 UK / 🇦🇺 AU | *"Turn base, report final."* |

In all regions a **Report Final** button then appears; your landing clearance is issued when you report final (an aircraft that was extended never received one at downwind).

### Orbit

A 360-degree turn in place, used for heavier IFR conflicts.

| Region | Instruction | Direction |
|---|---|---|
| 🇺🇸 US | *"Make a right three-sixty."* | Opposite to circuit direction |
| 🇬🇧 UK | *"Orbit right."* | Opposite to circuit direction |
| 🇦🇺 AU | *"Orbit right."* | Opposite to circuit direction |

### Circuit Breakout

If your extend or orbit lasts too long (due to continuous traffic), ATC may instruct you to report back to the downwind:

| Situation | What happens |
|---|---|
| **After an extended downwind** (about two minutes) | ATC breaks you out of the circuit: *"Turn right, rejoin and report downwind, due to traffic"* (US: *"turn right, re-enter and report midfield downwind, due to traffic"*). You re-enter the circuit from scratch. |
| **After an extended orbit** (about three minutes) | ATC advises that the airport is busy. US: *"Airport very busy, delay is not determined. You may want to depart the area and come back at another time."* UK/AU: *"Extended delay due to traffic volume. You may wish to depart the circuit and return later."* Your orbit continues and the advisory can repeat. |

### Go Around

If the runway becomes unavailable while you are on final, ATC will issue a go-around instruction. You will re-enter the circuit from the beginning.

| Region | Instruction |
|---|---|
| 🇺🇸 US | *"Go around, make left traffic."* |
| 🇬🇧 UK | *"Go around, I say again, go around. Make left hand circuit."* |
| 🇦🇺 AU | *"Go around, make left circuit."* |

!!! note "Note"
    You can also call a go-around yourself: say *"going around"* at any point after your downwind report, or use the **Go Around** button once you are in the landing phase. ATC gives you a circuit re-entry with a report instruction:

    | Region | Response |
    |---|---|
    | 🇺🇸 US | *"Roger, make left traffic, runway 27, report midfield downwind."* |
    | 🇬🇧 UK | *"Roger, go around acknowledged. Make left hand circuits, runway 27, report downwind."* |
    | 🇦🇺 AU | *"Roger, go around. Make left circuit, runway 29, report turning base."* |

---

## Runway & Direction Changes

### Changing Your Runway

You can request a different runway when another active runway is available: on the ground after your taxi instructions and before you report ready for departure, or in the air after your join clearance and before your landing clearance.

| When | What happens |
|---|---|
| **Before departure** (on the ground) | Use the "Request Runway Change" button and pick a runway from the sub-menu; ATC re-issues taxi instructions for the new runway. Asking by voice always gets *"say preferred runway"* first; answer with the runway or a button. |
| **During arrival** (in the circuit) | ATC will re-sequence you for the requested runway. |

For button users, a sub-menu shows the available active runways when using buttons.

### Changing Your Circuit Direction

!!! note "Default circuit direction"
    Unless there is a conflict with an active runway, or terrain, BeyondATC will default to the left for circuit directions.

If you are doing circuits, you can request the opposite circuit direction on the ground (after departure clearance) or in the air (after join clearance). Use the button (**Request Right Traffic** in the US, **Request Right Circuits** in the UK, **Request Right Circuit** in Australia) or say *"Request right traffic"* / *"Request right circuit"*.

ATC will acknowledge and re-issue your clearance with the updated direction. Regional wording:

| Region | Response |
|---|---|
| 🇺🇸 US | *"Right traffic approved."* |
| 🇬🇧 UK | *"Right hand circuits approved."* |
| 🇦🇺 AU | *"Right circuit approved."* |
