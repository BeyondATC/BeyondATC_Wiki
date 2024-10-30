---
hide:
  - navigation
  - toc

og_image: https://wiki.beyondatc.net/assets/cards/card-airport-ops.png
og_description: Airport standard operating procedures are used in BeyondATC to assign runways based on factors such as wind conditions and airport preferences. Currently, the airport SOPs implemented in BeyondATC are relatively simple in design, focusing primarily on essential factors.
description: Airport standard operating procedures are used in BeyondATC to assign runways based on factors such as wind conditions and airport preferences. Currently, the airport SOPs implemented in BeyondATC are relatively simple in design, focusing primarily on essential factors.

---

# How are airport SOPs implemented in BeyondATC

Airport standard operating procedures are used in BeyondATC to assign runways based on factors such as wind conditions and airport preferences. Here’s an example of how a preferential runway system for LSZH (Zurich) is defined:

```json
{
  "icao": "LSZH",
  "low_wind_speed": 7,
  "low_wind_runways": ["14", "28"],
  "primary_departing_runways": ["16", "28", "32"],
  "primary_arrival_runways": ["14", "16", "34"]
}
```

| Setting                     | Description                                                                                                                                                                                      |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Low wind speed**          | The wind speed threshold (in knots) for the preferential runway system. When the wind speed is below this threshold, specific low-wind runways are used.                                          |
| **Low wind runways**        | Runways used in calm wind conditions (when wind speed is below the defined low wind threshold) and during tailwind situations. These are the preferred runways in low-wind or tailwind scenarios. |
| **Primary departing runways**| Runways designated for departures. |
| **Primary arrival runways**  | Runways designated for arrivals.  |

If wind speeds are below the specified threshold (`low_wind_speed`), the system will choose runways from the list of `low_wind_runways` for both arrivals and departures, unless there is a stronger tailwind.

Currently, the airport SOPs implemented in BeyondATC are relatively simple in design, focusing primarily on essential factors such as wind conditions and runway assignments. However, there are plans to enhance and expand these procedures in the future to incorporate more complex decision-making processes and better simulate real-world operations.