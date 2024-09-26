---
hide:
  - navigation
  - toc
---

# How ATIS work in BeyondATC

**BeyondATC generates ATIS reports independently**, relying on weather data (METAR) from aviationweather.gov (+ VATSIM as a second source) and available airport operations provided by the community. This system mimics how real-world controllers make decisions but does not aim to replicate real-time ATIS. This can lead to differences between the ATIS you receive from BeyondATC and the active runways information provided by real-world sources or flight planning tools like Simbrief or Navigraph.

These discrepancies will be reduced in the future with the introduction of more advanced airport operations. Currently, BeyondATC's airport SOPs are relatively simple. They include and are limited to:

- Preferential low-wind runways for departures and arrivals (based on a specific low-wind threshold)
- Dedicated runways assigned for departures and/or arrivals

However, there are several limitations with the current system (not an exhaustive list):

- Multiple preferential runway systems based on time of day or wind direction cannot be defined
- For runways used for both departures and arrivals, it’s not possible to assign a low-wind preference exclusively to one operation (departure or arrival)
- Intersecting runways cannot both be active simultaneously
- Runways assigned to one aircraft type are not currently supported

These advanced features may be added in future updates. For now, these limitations may result in runway assignments that don’t fully align with real-world operations.

## Why BeyondATC does not follow the chosen runway in Simbrief?

Runway assignments in BeyondATC may not always match those in your Simbrief flight plan due to key differences in how each system handles runway selection. 

Simbrief creates flight plans based on forecasted weather conditions at the time of planning, which might not reflect real-time conditions by the time of your flight. Additionally, the actual runway in use at an airport is determined by multiple factors: current METAR weather data, ATC decisions based on traffic flow and safety, and airport standard operating procedures (SOPs) with their current limitations. Because of these dynamic, real-time variables, the runway specified in your Simbrief plan may differ from the one currently in use. It’s important to understand that ATC has the final say on active runway assignments, prioritizing safety and efficiency over pre-planned routes.

## Why don't BeyondATC use real-world sources for active runways?

There isn’t a reliable source available for every airport worldwide. The purpose of BeyondATC is not to replicate real-time ATIS, but to provide a consistent and immersive experience within a simulated environment. In the event that historic weather support is added, real-world sources wouldn’t resolve the issue as runway assignments would still need to be generated independently.