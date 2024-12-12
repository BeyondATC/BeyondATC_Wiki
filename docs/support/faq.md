---

og_image: https://wiki.beyondatc.net/assets/cards/card-faq.png
og_description: Find all frequently asked questions about BeyondATC and their answers.
description: Find all frequently asked questions about BeyondATC and their answers.

---

# Frequently asked questions

## General questions

???+ info "What does Early Access mean?"
    Early Access is way for you to purchase and use the program before it is complete. This approach enables users to participate in the final development stages by providing feedback, reporting bugs, and suggesting improvements. In return, users get a chance to explore new features ahead of the final release.

    **This means if you purchase BeyondATC, you are getting a program still under development. This program will include bugs and strange behavior. Please make sure you understand this before making your purchase decision.**

??? info "How much does BeyondATC cost?"
    The basic pack is priced at $29.99. This pack includes all core features, with no additional purchases required unless you choose to buy Premium Characters for enhanced voice options. Additionally, a Supporter Pack is available for $59.99 if you want to support our development, granting access to the experimental branch where new features are introduced first for testing as a thank you.

    For detailed information on pricing and available options, please visit our [pricing page](../onboarding/pricing.md).

??? info "Is BeyondATC a one-time purchase?"
    Yes! BeyondATC comes with a large amount of Premium Characters included in the base purchase (about an hour of speaking time), and that is yours to use from the moment you purchase the product. However, you are not required to use this voice model at all. The product works entirely from start to finish with the Basic Voice Model, and requires no additional purchases of any kind. Additionally, it will include all future updates and upcoming features!

??? info "What is the Supporter's Pack?"
    The Supporter's Pack is a pack that you can buy to support the development of BeyondATC. We give access to the experimental branch as a 'thank you' to our users so you get something fun in return for your donation. What the experimental branch is NOT is a paywall for features. All features that start in experimental will end up in the public branch. So we want to encourage all users to think of the Supporter's Pack in this way - please do not purchase the Supporter's Pack to get a single feature. Do so only if you want to support our development. 

??? info "Is BeyondATC powered by AI?"
    We use the latest in AI technologies to process your voice, decide what the ATC should do, and generate highly realistic responses with AI voices. However, to keep the program affordable we do not use a LLM (Large Language Model) such as Gemini or ChatGPT.

??? info "Does BeyondATC require an active internet connection?"
    Yes, our voices use cloud-based technology and require an active connection to work.

??? info "Which simulators is BeyondATC be available for?"
    BeyondATC is designed for Microsoft Flight Simulator 2020 and 2024 on PC.

    We have not planned to support any other simulator or platform. It is technically not possible to support Xbox.

??? info "Is there a trial period?"
    We do not offer a trial period at this stage. You can search for BeyondATC videos and review to make your decision.

??? info "Is BeyondATC powered by AI?"
    We use the latest in AI technologies to process your voice, decide what the ATC should do, and generate highly realistic responses with AI voices. However, to keep the program affordable we do not use a LLM (Large Language Model) such as Gemini or ChatGPT.

??? info "Do I need a Navigraph subscription to use BeyondATC?"
    You don’t need a Navigraph subscription to use BeyondATC. The software pulls information directly from your simulator, including airport data, approaches, waypoints, and more, using the scenery and AIRAC cycle already available in your sim. However, if you generate a flight plan in Simbrief using a different AIRAC cycle than what’s in your simulator, you may encounter specific discrepancies.

    If desired, you can opt for a one-month Navigraph subscription to update both your simulator and Simbrief with the latest AIRAC cycle, ensuring everything is synchronized to the same source.

## Features

??? info "How can I load a new flight plan for my next flight?"
    You can load a new flight plan by using the escape key in BeyondATC. It will bring you to the main menu where you can load your new flight.

??? info "Are diversions supported?"
    Diversions are not supported at the moment and might be added later as part of the emergencies procedures. However, there is a workaround that you can use to make a diversion in the meantime:

    - Enter in a holding pattern if necessary
    - File a new Simbrief flight plan to your diversion airport
    - Hit the escape key in BeyondATC to go back to the main menu
    - Load your new flight plan and choose the correct flight phase
    - You will be told to be off course and given a new direct to. Go direct to this fix and continue your flight to the alternate airport.

??? info "Can I request a different approach?"
    At the moment, it is not possible to change the approach you are assigned by ATC. This is a feature that is planned for later.

## ATC questions

??? info "Why am I regularly getting Squawk 1000?"
    Squawk 1000 is used between a few countries in Europe as part of a modernized air traffic management system. This code is specifically tied to the use of Mode S transponders, which provide detailed aircraft information, such as position and unique identifier, directly to air traffic controllers. Unlike traditional squawk codes, which require different codes for different flights, squawk 1000 simplifies the process by standardizing the code for all aircraft equipped with Mode S.

    Countries Using Squawk 1000

    - Austria
    - Belgium
    - Croatia
    - Czech Republic
    - France
    - Germany
    - Hungary
    - Italy
    - Luxembourg
    - Netherlands
    - Poland
    - Romania
    - Slovakia
    - Switzerland (LSZR,LSZB,LSZG,LSGC,LSZH,LSGG)

    **This behavior is modeled in BeyondATC. Therefore, you will be assigned squawk 1000 if you are flying between these countries.**

    For more info:

    - [https://forums.vatsim.net/topic/27699-squawk-1000/](https://forums.vatsim.net/topic/27699-squawk-1000/)
    - [https://www.pprune.org/atc-issues/484742-squawk-1000-a.html](https://www.pprune.org/atc-issues/484742-squawk-1000-a.html)
    - [https://skybrary.aero/articles/mode-s](https://skybrary.aero/articles/mode-s)

??? info "Why BeyondATC makes me use a runway that is not active in real life?"
    **BeyondATC generates ATIS reports independently**, relying on weather data (METAR) from aviationweather.gov (+ VATSIM as a second source) and available airport operations provided by the community. This system mimics how real-world controllers make decisions but does not aim to replicate real-time ATIS. This can lead to differences between the ATIS you receive from BATC and the active runways information provided by real-world sources or flight planning tools like Simbrief or Navigraph.

    These differences will be minimized in the future thanks to more complex airports operations. Currently, BATC's airports SOPs are basic. They include:
    
    - Preferential low wind runways used for departures and arrivals (based on a low-wind threshold)
    - Defined runways for departures and/or arrivals

    Advanced features such as curfews, time-based runway changes, or direction-specific runway assignments are not yet implemented. 

??? info "Should ATC instruct me when I have to descend?"
    As the pilot in command, **it is your responsibility to request descent when needed**. While ATC typically prompts you to descend, there may be times when they don't, or when their instruction comes later than you require. This can happen for several reasons, one being that ATC does not have precise knowledge of your TOD. The TOD is specific to your aircraft's performance and the descent planning you've calculated, which ATC cannot determine. Therefore, it’s essential to monitor your descent profile and, when necessary, report that you are ready for descent so ATC can issue the appropriate clearance.

    You can read our [Beginner Guide about descent planning](../../beginner-guide/cruise/#descent-planning) if you need help.

??? info "Why isn't BeyondATC using the runway specified in my flight plan?"
    In real-world aviation, runways are not pre-assigned in flight plans. Instead, they are determined by Air Traffic Control (ATC) based on current conditions like wind direction, runway availability, and traffic volume.

    SimBrief provides a suggested runway based on standard conditions at the time of planning, but the actual runway assignment can change when you’re closer to your departure or arrival. BeyondATC simulates this real-world ATC behavior by assigning runways dynamically, just as in actual flight operations.

??? info "Why is BeyondATC directing me to use incorrect taxiways?"
    BeyondATC relies on airport scenery data for taxiway routing, but currently, it doesn't use taxiway width information. This is because, in both third-party and default sceneries, taxiway sizing is often inaccurate or inconsistently defined. Attempting to use this incomplete data would likely lead to more routing issues, so BeyondATC focuses on the best available information without relying on potentially unreliable taxiway width data.

## AI Traffic

??? info "What is the traffic source?"
    BeyondATC uses data from FlightRadar24, using a historic week of data. This includes all IFR flights, GA included. 

??? info "Why are you not using live traffic? Are you planning to add it later?"
    Various factors were evaluated such as costs, contracts, user feedback, system architecture, and development timeline. Based on these criteria, the choice was made not to use live traffic data.

    Tests showed minimal differences that most users won't notice. This setup offers a seamless experience without the complexities and costs of live traffic, allowing users to choose their flight times and experience busy airports.

    Currently, there are no plans to implement live traffic or support any other injectors. 

??? info "Will you update the traffic data?"
    We plan to update the dataset to provide more relevant traffic data for the simulator. However, please keep in mind that this data is costly, and while we are committed to making updates, we currently do not have a specific timeline for when this will happen as it has to be discussed with the data provider. 

??? info "Which models will BeyondATC use for AI Traffic?"
    BeyondATC will use whatever models you have installed in your simulator, including any combination of AIG, FSLTL, and FS Traffic.

??? info "BeyondATC says that no traffic liveries are found"
    Make sure you have installed models for at least one provider (AIG, FSLTL or FS Traffic) in the community folder of the MSFS version you are using. If it still doesn't work, start BeyondATC as an administrator.

??? info "Can BeyondATC use the new traffic models that come with MSFS 2024?"
    The new traffic models included with MSFS 2024 currently do not support external injection outside of the simulator’s default traffic engine. We are investigating this further, but as of now, they may not be usable by third-party applications. Updates will follow as we learn more.

??? info "Can AI traffic use ground services?"
    Currently, AI traffic can utilize pushback tugs injected by BeyondATC. However, injected AI aircraft are not yet able to use jetways. This functionality requires an update from Asobo to enable third-party software to trigger jetway operations for non-player aircrafts.

??? info "What features are available with AI Traffic?"

    - A **custom built injector** just for BeyondATC using a comprehensive 3D simulation of every plane's logic and movement.
    - **Flight operations from all over the world**, boasting over 1 million+ flights from every part of the globe.
    - **Gate-accurate airlines** for every airport.
    - **Airframe performance calculations**, meaning each airframe type will takeoff, land, bank, and pitch according to its performance characteristics.
    - **Full integration of traffic into the ATC system**. All aircraft and ATC will call in and make requests for every stage of flight, accurate to its real world flight plan using the same system as the player.
    - **Aircraft agnostic preferencin**g - BeyondATC doesn't know the difference between the player's aircraft and traffic meaning it will handle and prioritize your plane in the same way it does traffic making for a very realistic simulation of action priority.
    - **Taxi logic** which will reserve paths along the airport and give way to passing aircraft, resulting in many fewer "standoff situations" than default traffic where aircraft will end up facing each other along a taxiway, unable to move.
    - **Runway logic and simulation**, aircraft are told to line up, hold short, cross runways (with a higher priority the longer they are waiting) and are given clearance according to a deep runway logic simulation. Runway simulation accounts for wake turbulence according to airframe, waiting for vortices to clear before releasing an aircraft for takeoff. An aircraft will be warned of wake turbulence if the preceding aircraft is of a larger airframe than its own.
    - **"Bird's Eye Airport Logic"** where each controller of an airport has situational awareness of what's happening in other sectors of the airport, coordinating their actions according to others situations.
    - **Full traffic representation** for all stages of flight; clearance, pushback, taxi, takeoff, departure, center, approach, landing, taxi in, shut down.
    - **Traffic go arounds**: traffic will be told to go around if the landing runway is occupied or unsafe. The traffic then flies the full vectored circuit back to the IAF where it will attempt another landing. The player will also be told to go around if traffic is on the runway or the runway deemed unsafe.
    - **Multi-Frequency airport comms**: airports are broken up into multiple comm frequencies as determined by custom ops data. This keeps comms clear and contextual to which runway the comm is assigned. (Data for this feature is continuing to be expanded. Currently we have data for about 25 airports).
    - **Airplane sequencing**, aircraft will be sequenced in to maintain a distance between them according to their speed and airframe. The player is included in these calculations. 
    - **Pushback tugs**, tugs will pushback the aircraft from the gate.
    - **Custom takeoff and landing animations**, these animations are custom built per airframe. Aircraft will flare on landing, and pitch up before lifting off on takeoff. We believe no other traffic injector, including the MS default injector matches the quality and breadth of these animations.
    - **Full integration of traffic into the local BeyondATC airport map**, and a wider view enroute traffic map which can be downloaded [here](https://www.beyondatc.net/download).

??? info "How do I set up everything to use traffic with BeyondATC?"
    Please follow our setup guide [here](../../onboarding/getting-started)

??? info "There is not enough traffic"
    BeyondATC uses historical FR24 data, so traffic density may not always meet your expectations. Here are a few factors that might explain variations in traffic:  

    1. **Seasonal variations**: Traffic density can be affected by the time of year, especially at airports with significant seasonal changes in activity. The data represents one week from earlier this year.  
    2. **Simulator time**: Traffic is loaded according to the simulator's time setting. For example, if you spawn at night at an airport, you might see less traffic or no movement due to curfews.  
    3. **Model installation**: Ensure your models are correctly installed. If a model is missing, fewer aircraft will be injected into the simulator.  

??? info "Traffic is not moving"
    Injected aircraft will begin moving once they reach their scheduled departure time. It may take a little while before you notice movement at the airport.

??? info "Can traffic backtrack on a runway?"
    At the moment, traffic cannot backtrack on a runway. You might experience weird traffic behaviors in airports where backtracking is mandatory.


## Troubleshooting issues

??? info "Why can't I type anything in the Simbrief ID field?"
    Make sure you are typing your **Pilot ID** and not your username. It should be numbers only.

??? info "I can't reset my password. It says that it's unable to generate a password reset link."
    Please send a email to support@beyondatc.net with your username and a copy of your receipt to request a manual reset.

??? info "I can't log into my account"
    Make sure you are using the correct username. **Usernames are case sensitive.**

    You can reset your password with the "forgot my password" button in BeyondATC. If this doesn't work or you created an account without an email please email support@beyondatc.net with a copy of your receipt.

??? info "Why are my frequencies switching back to something else?"
    You need to disable ATC assistance options in MSFS settings. Please have a look at [our guide](../../onboarding/getting-started/#setting-up-ai-traffic) to set everything up correctly.

??? info "Simbrief cannot be reached. What can I do?"
    Make sure you have filed a flight plan in Simbrief and Detailed Navlog is checked.

??? info "BeyondATC freezes when I press my PTT button."
    This happens when BeyondATC can't access your microphone. If you have that issue:

    - Check that your microphone is connected and working
    - Go to Settings > Privacy and security > Microphone and check that apps are allowed to use the microphone (at the bottom of the section)
    - Open BATC, disconnect and reconnect your microphone

??? info "Why is BeyondATC telling me that a runway does not exist?"
    BeyondATC uses data directly from MSFS scenery, so if a scenery is outdated or differs from what tools like SimBrief reference, it may result in runway discrepancies. BeyondATC can account for minor changes, such as a one-digit difference in runway numbers, but significant changes—like renaming 06 to 06L—are not recognized and will cause this error.

    To solve this error, you need to check if a custom scenery is available and up to date.