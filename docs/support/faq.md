# Frequently asked questions

## General questions

???+ info "What does Early Access mean?"
    Early Access is way for you to purchase and use the program before it is complete. This approach enables users to participate in the final development stages by providing feedback, reporting bugs, and suggesting improvements. In return, users get a chance to explore new features ahead of the final release.

    **This means if you purchase BeyondATC, you are getting a program still under development. This program will include bugs and strange behavior. Please make sure you understand this before making your purchase decision.**

??? info "How much does BeyondATC cost?"
    The basic pack is priced at $29.99. This pack includes all core features, with no additional purchases required unless you choose to buy Premium Characters for enhanced voice options. Additionally, a Supporter Pack is available for $59.99, granting access to the experimental branch where new features are introduced first for testing.

    For detailed information on pricing and available options, please visit our [pricing page](../onboarding/pricing.md).

??? info "Is BeyondATC a one-time purchase?"
    Yes! BeyondATC comes with a large amount of Premium Characters included in the base purchase (about an hour of speaking time), and that is yours to use from the moment you purchase the product. However, you are not required to use this voice model at all. The product works entirely from start to finish with the Basic Voice Model, and requires no additional purchases of any kind. Additionally, it will include all future updates and upcoming features!

??? info "Does BeyondATC require an active internet connection?"
    Yes, our voices use cloud-based technology and require an active connection to work.

??? info "Which simulators is BeyondATC be available for?"
    BeyondATC is currently designed for Microsoft Flight Simulator 2020 and is also planned to support the upcoming 2024 edition.

    We have not planned to support any other simulator.

??? info "Is there a trial period?"
    We do not offer a trial period at this stage. You can search for BeyondATC videos and review to make your decision.

??? info "Is BeyondATC powered by AI?"
    We use the latest in AI technologies to process your voice, decide what the ATC should do, and generate highly realistic responses with AI voices. However, to keep the program affordable we do not use a LLM (Large Language Model) such as Gemini or ChatGPT.

??? info "Do I need a Navigraph subscription to use BeyondATC?"
    You don’t need a Navigraph subscription to use BeyondATC. The software pulls information directly from your simulator, including airport data, approaches, waypoints, and more, using the scenery and AIRAC cycle already available in your sim. However, if you generate a flight plan in Simbrief using a different AIRAC cycle than what’s in your simulator, you may encounter specific discrepancies.

    If desired, you can opt for a one-month Navigraph subscription to update both your simulator and Simbrief with the latest AIRAC cycle, ensuring everything is synchronized to the same source.

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

## Troubleshooting issues

??? info "Why can't I type anything in the Simbrief ID field?"
    Make sure you are typing your **Pilot ID** and not your username. It should be numbers only.

??? info "I can't reset my password. It says that it's unable to generate a password reset link."
    Please send a email to support@beyondatc.net with your username and a copy of your receipt to request a manual reset.

??? info "I can't log into my account"
    Make sure you are using the correct username. **Usernames are case sensitive.**

    You can reset your password with the "forgot my password" button in BeyondATC. If this doesn't work or you created an account without an email please email support@beyondatc.net with a copy of your receipt.

??? info "Why are my frequencies switching back to something else?"
    You need to disable ATC assistance options in MSFS settings. Please have a look at [our guide](../onboarding/getting-started/) to set everything up correctly.

??? info "Simbrief cannot be reached. What can I do?"
    Make sure you have filed a flight plan in Simbrief and Detailed Navlog is checked.

??? info "BeyondATC freezes when I press my PTT button."
    This happens when BeyondATC can't access your microphone. If you have that issue:

    - Check that your microphone is connected and working
    - Go to Settings > Privacy and security > Microphone and check that apps are allowed to use the microphone (at the bottom of the section)
    - Open BATC, disconnect and reconnect your microphone
    
??? info "BeyondATC cannot connect to the simulator"
    Fistly, ensure the simulator is running at least as far as the main menu, preferably with you on the ground at your departure airport. If the issue persists trying the following steps, retrying to use BATC after each step:

    1. Restart MSFS and BeyondATC - check task manager also and make sure any simconnect_ws.exe process is killed if still running after BATC is closed.
    2. Ensure your antivirus and firewall are not blocking BATC from connecting to the internet.
    3. Run BeyondATC as admin
    4. Restart your PC
    5. Uninstall BeyondATC, redownload from the website and install as admin
    6. While BATC is still open, return to Main Menu in MSFS and retry BATC. It should display a message "The connection to the simulator has been lost". Spawn into the airport again and when ready, BATC should connect.
    7. Alternatively, start BATC when in Main Menu. Before spawning at airport.
    8. Try using a VPN (users from Turkey and Hong Kong may have issues using the software without)
    9. Check if your Antivirus or Windows Security blocked any file from BeyondATC (especially the simconnect file). You will need to restore it to allow BATC to connect to the simulator. Then, add the entire BATC folder as an exception.