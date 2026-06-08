---
hide:
  - navigation
  - toc

og_description: Live Traffic injects real-world aircraft into your sim in their actual, current positions using Navigraph's real-time traffic data. Learn how to link Navigraph, turn it on, and what to expect.
description: Live Traffic injects real-world aircraft into your sim in their actual, current positions using Navigraph's real-time traffic data. Learn how to link Navigraph, turn it on, and what to expect.

---

# Live Traffic (Experimental Feature)

**Live Traffic** fills your skies and airports with the aircraft that are *actually flying right now* in the real world. Instead of replaying a recorded week of schedules, BeyondATC pulls live positions from **Navigraph's real-time traffic** and builds the traffic around you from what's genuinely up there at this moment.

That means when you push back at your departure airport, the aircraft you taxi past, the jet that lands ahead of you, and the traffic you hear on frequency are the real flights operating that route today — same callsigns, same aircraft types, same airlines.

!!! info "How it differs from standard (scheduled) traffic"
    Standard BeyondATC traffic is built from a **historic week** of real schedule data and is driven by the time of day you set in the sim. **Live Traffic** is built from **what is flying at this exact moment**, streamed live. The two work together: BeyondATC still seeds your departure airport with parked aircraft from the schedule so the ramp looks nice and full, and Live Traffic then **takes over those aircraft or adds to them** as the real-world flights call for it.

---

## What you need

To use Live Traffic you need three things in place:

1. **A Navigraph Unlimited subscription** — Live Traffic is powered by Navigraph's real-time traffic data, which is part of their **Unlimited** subscription. You can check your plan or upgrade on the [Navigraph website](https://navigraph.com).
2. **Your Navigraph account linked to BeyondATC** — see below.
3. **AI traffic models installed** — exactly like standard traffic, BeyondATC does **not** ship aircraft models. You need models from one of the supported sources:
    - FSLTL
    - Alpha India Group (AIG)
    - FS Traffic
    - BravoAirspace Airline Traffic Global (ATG) *(MSFS 2024 only)*

    You must **not** run any injector from these packages — BeyondATC handles injecting the aircraft.

    !!! tip "BravoAirspace ATG on MSFS 2024"
        BravoAirspace ATG uses the simulator's built-in (native) traffic models, so it's available on **MSFS 2024** only. 

---

## Linking your Navigraph account

Live Traffic needs your Navigraph account linked to BeyondATC. There are two ways to start it — both open the same quick browser sign-in:

- **From the Live Traffic toggle (easiest)** — just switch **Live Traffic** on in the traffic options (see below). If you aren't linked yet, BeyondATC opens the Navigraph linking page for you automatically.
- **From the Account window** — open the **Account** window, find the **Navigraph** row and click **Link**.

Either way, the sign-in is the same:

1. Your browser opens to a Navigraph page showing a short code. Sign in to Navigraph and enter the code to authorise BeyondATC.
2. Back in BeyondATC the status changes to **Linked**. The link is remembered, so you only need to do this once.

!!! tip "Staying linked"
    Once linked, BeyondATC keeps the connection alive in the background. If you ever want to disconnect, use the **Unlink** button in the Account window's Navigraph row.

---

## Turning Live Traffic on

1. Open **Options** and go to the **Traffic** settings.
2. Switch on the **Live Traffic** toggle.

If you're **already linked** to Navigraph, that's it — on your next flight BeyondATC populates the world from the live feed.

If you're **not linked yet**, switching it on won't enable it straight away — instead BeyondATC opens the Navigraph linking page in your browser. Once you've finished linking, switch the toggle on again and it will stay on.

!!! note "The toggle won't stay on"
    Live Traffic can't run without a live data source, so the switch only stays on once your Navigraph account is linked. Flipping it on while unlinked kicks off the linking process for you. After you link, switch it on again and it works normally.

!!! warning "Set your sim clock to real-world time"
    Live Traffic only makes sense when your simulator's clock matches the **real-world time right now**. If your sim time is set to live/real time, everything lines up. If it's set to a different time, BeyondATC will warn you when you start your flight and give you the choice to **continue anyway** or **disable Live Traffic for that flight**. For the best experience, fly with your sim set to live time.

---

## What Live Traffic does

- **A full, real airport** — your departure airport is seeded with parked aircraft from the schedule so the ramp looks busy, and Live Traffic then takes over those airframes (or adds new ones) to match what's really happening on the ground.
- **Real positions as a starting point** — airborne aircraft are placed where the real flights actually are when they come into range. From there BeyondATC takes control and flies them, so they may drift from the exact real-world track — though in practice usually not by much.
- **Real departures** — a parked aircraft only departs when its real-world counterpart actually starts moving on the ground. If a real flight is already taxiing when you load in, BeyondATC drops it onto the taxiway where it really is.
- **Arrivals and enroute traffic** — aircraft inbound to your airports, and traffic passing through the area around you, are brought in based on the live feed, nearest to you first.
- **Coverage around you** — BeyondATC manages live traffic in a bubble around your aircraft (out to roughly 200 nm), and that bubble grows as you climb, so you still get traffic at cruise.
- **Your density sliders still apply** — the Parked, Departures, Arrivals and Enroute sliders work exactly as they do for standard traffic, so you stay in control of how busy things get. See [How the traffic sliders work](traffic-slider.md).

---

## What Live Traffic doesn't do

Live Traffic is about *who* is flying and *where they are*, not a perfect recreation of every real-world flight plan. A few things to be aware of:

- **It doesn't fly the exact real filed route.** The live feed provides each aircraft's position, callsign, type and origin/destination — but **not** its actual filed route. BeyondATC uses the real position as a starting point and then flies the aircraft itself along a sensible route between the two airports, so its exact track and cruise altitude can drift from the real flight. In practice the difference is often small, but it can be more noticeable on long-haul.
- **It isn't a continuous live mirror.** Positions refresh every 20–60 seconds, so traffic moves on BeyondATC's own smooth path between updates rather than being a frame-by-frame copy of the real world.
- **Live traffic always runs on real-world time, not your sim time.** The initial parked aircraft that seed your airport come from BeyondATC's schedule and match the time of day set in your sim — but everything live is whatever is genuinely flying right now in the real world. The two only line up when your sim clock is set to live/real time. If they're far apart you'll get an odd mix: for example, fly with your sim set to 3 PM while it's 3 AM at that airport in real life and the ramp will look busy from the scheduled parked aircraft, but there'll be very little live traffic actually moving, because hardly anything is flying there at that hour.
- **It won't inject your own flight.** If you're flying a real-world callsign that also appears in the live feed, BeyondATC excludes it so you never see a copy of yourself.
- **It still needs traffic models.** No models in your community folder means no aircraft to show — just like standard traffic.

!!! info "A reminder on intent"
    Live Traffic is here to give you realistic, current traffic to share the skies with — not a pixel-perfect plane-spotting mirror of the real world. If a particular flight's route or timing isn't exact, that's expected.

---

## Troubleshooting

??? question "The Live Traffic toggle won't stay on"
    Your Navigraph account isn't linked yet. Switch the toggle on once to open the Navigraph linking page automatically (or link from the **Account** window), complete the sign-in, then switch Live Traffic on again — it will now stay on.

??? question "I turned it on but I don't see any live traffic"
    Check the following:

    - You're **linked** to Navigraph and have a **Navigraph Unlimited** subscription (required for real-time traffic).
    - You have **traffic models** installed (FSLTL, AIG, FS Traffic, or BravoAirspace ATG on MSFS 2024).
    - Your **sim clock is set to real-world time** — at an off time there may genuinely be little or no matching real traffic.
    - Your **density sliders** aren't all at zero.
    - You launched BeyondATC **as administrator**.

    For more general traffic issues, see [No AI traffic](../support/common-issues/notraffic.md).

??? question "The aircraft aren't flying the routes I'd expect"
    This is expected — the live feed doesn't include real filed routes, so BeyondATC generates its own. See [What Live Traffic doesn't do](#what-live-traffic-doesnt-do) above.

If you're still stuck, please share your log files in our [Discord](https://discord.gg/beyondatc).
