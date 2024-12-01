---
hide:
  - navigation
  - toc

og_image: https://wiki.beyondatc.net/assets/cards/card-airport-ops.png
og_description: Airport standard operating procedures are used in BeyondATC to assign runways based on factors such as wind conditions and airport preferences. Currently, the airport SOPs implemented in BeyondATC are relatively simple in design, focusing primarily on essential factors.
description: Airport standard operating procedures are used in BeyondATC to assign runways based on factors such as wind conditions and airport preferences. Currently, the airport SOPs implemented in BeyondATC are relatively simple in design, focusing primarily on essential factors.

---

# How are airport SOPs implemented in BeyondATC

Airport standard operating procedures are used in BeyondATC to assign runways based on factors such as wind conditions and airport preferences. Here’s an example of how airport data is defined for KLAX (Los Angeles):

``` json
{
  "icao": "KLAX",
  "low_wind_speed": 5,
  "low_wind_runways": ["24L", "24R", "25L", "25R"],
  "primary_departing_runways": ["25R", "24L", "07L", "06R"],
  "primary_arrival_runways": ["25L", "24R", "06L", "07R"],
  "frequencies": [
    {
      "runway": ["24L", "24R", "06R", "06L"],
      "tower": {
        "name": "Los Angeles",
        "frequency": 133.9
      },
      "ground": {
        "name": "Los Angeles",
        "frequency": 121.65
      },
      "departure": {
        "name": "SOCAL",
        "frequency": 125.2
      },
      "approach": {
        "name": "SOCAL Approach",
        "frequency": 124.5
      }
    },
    {
      "runway": ["25L", "25R", "07L", "07R"],
      "tower": {
        "name": "Los Angeles",
        "frequency": 119.8
      },
      "ground": {
        "name": "Los Angeles",
        "frequency": 121.75
      },
      "departure": {
        "name": "SOCAL",
        "frequency": 124.3
      },
      "approach": {
        "name": "SOCAL",
        "frequency": 124.9
      }
    }
  ]
}
```

| Setting                      | Description             |
| ---------------------------- | ----------------------- |
| **Low wind speed**           | The wind speed threshold (in knots) for the preferential runway system. When the wind speed is below this threshold, specific low-wind runways are used. |
| **Low wind runways**         | Runways used in calm wind conditions (when wind speed is below the defined low wind threshold) and during tailwind situations. These are the preferred runways in low-wind or tailwind scenarios. |
| **Primary departing runways**| Runways designated for departures. |
| **Primary arrival runways**  | Runways designated for arrivals. |
| **Frequencies**              | This section groups communication frequencies based on the runway groups to separate communication between multiple frequencies in bigger airports. |

If wind speeds are below the specified threshold (`low_wind_speed`), the system will choose runways from the list of `low_wind_runways` for both arrivals and departures, unless there is a stronger tailwind.

Currently, the airport SOPs implemented in BeyondATC are relatively simple in design, focusing primarily on essential factors such as wind conditions and runway assignments. However, there are plans to enhance and expand these procedures in the future to incorporate more complex decision-making processes and better simulate real-world operations.