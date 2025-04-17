---
hide:
  - navigation
  - toc

og_image: https://wiki.beyondatc.net/assets/cards/card-airport-ops.png
og_description: Airport standard operating procedures are used in BeyondATC to assign runways based on factors such as wind conditions and airport preferences.
description: Airport standard operating procedures are used in BeyondATC to assign runways based on factors such as wind conditions and airport preferences.

---

# How are airport SOPs implemented in BeyondATC

Standard Operating Procedures (SOPs) in BeyondATC allow each airport to dynamically select the most appropriate arrival and departure runways based on real-world-like logic. These procedures replicate local preferences and constraints while adapting to live weather, time, and traffic conditions.

---

## 🧠 How the SOP system works

The SOP system evaluates a set of flows—predefined configurations that dictate which runways are used for arrivals and departures under certain conditions. The system continuously checks for the best matching flow based on the following criteria:

1. **Wind direction and speed**
2. **Time of day**
3. **Day of the week**
4. **Aircraft type**

Once a match is found, BeyondATC applies the runways defined in that flow for all arriving and departing traffic.

---

## 📦 Flow structure

Each SOP flow is defined using the following parameters:

| Parameter         | Description                                                                |
|------------------|-----------------------------------------------------------------------------|
| `name`            | A label for the flow (used internally and for debugging/logging)           |
| `day_range`       | Days when the flow is active (`0 = Sunday`, ..., `6 = Saturday`)           |
| `time_range`      | Time range during which the flow is valid (in 24h format)                  |
| `wind_dir`        | Wind direction range                                                       |
| `wind_speed`      | Acceptable wind speed range (in knots)                                     |
| `arrival_runways` | Runways to be used for arrivals                                            |
| `departing_runways` | Runways to be used for departures                                        |
| `aircraft_type`   | If specified, applies only to these types (e.g. `heavy_jet`, `light_jet`)  |

> 📝 The more specific the flow, the higher its priority when evaluating.

## ✈️ Aircraft Categories

SOPs can define restrictions for specific types of aircraft. The following categories are recognized:

- `light_prop`
- `medium_prop`
- `heavy_prop`
- `light_turboprop`
- `medium_turboprop`
- `light_jet`
- `medium_jet`
- `heavy_jet`
- `super_jet`

880 individual aircraft types (i.e. different icao codes) are all put into one of those categories. This is especially useful when an airport restricts certain runways to lighter or heavier aircraft (e.g., at LSZH, RWY 16 is used only by heavy and super jets for departure).

---

## 💡 Example: How it all comes together

Let’s say these two flows are defined at the airport:

```json
{
  "name": "North Concept",
  "day_range": [1, 2, 3, 4, 5],
  "time_range": ["07:00", "21:00"],
  "wind_speed": [0, 6],
  "wind_dir": [0, 360],
  "arrival_runways": ["14"],
  "departing_runways": ["28"]
}
```

```json
{
  "name": "South Wind Operations",
  "wind_speed": [6, 100],
  "wind_dir": [120, 210],
  "arrival_runways": ["34"],
  "departing_runways": ["28"],
  "aircraft_type": []
}
```

In this case:
- If winds are calm, it will choose a the standard flow (North concept) for low-wind situations during the defined day and time. This can result in a low tailwind until the wind speed exceed the low wind treshold set for this airport (6kt in this case)
- If the wind is from 180° at 14 kt, it will switch to the South Wind Operations, which will now have the priority as all its criteria are met.

---

## ⚠️ Limitations & Real-World Differences

While BeyondATC SOPs are designed to closely mirror real-world procedures, there are a few limitations to keep in mind:

- **Live ATC decisions** can change runway usage in real life on short notice due to traffic volume, noise abatement, runway closures, or airspace coordination. BeyondATC does not currently replicate those operational decisions dynamically.
- **Weather modeling** in BeyondATC relies on available METAR data and simplified interpretation. Real controllers might anticipate wind shifts or apply runway changes more proactively.
- **Runway preferences** may vary between airlines, time slots, or for sequencing efficiency. BeyondATC uses standardized logic, not airline-specific procedures.
- **Special operations** like parallel departures, SID/STAR preferences, or deicing constraints are not yet dynamically modeled.

**These SOP flows are a best-effort simulation of reality, optimized for a smooth user experience and realistic traffic flow—but they won’t always match what’s happening at the actual airport in real time.**

If you believe a SOP is wrong or could be improved, please share your log file and suggestion in [our support channel on Discord](https://discord.com/channels/1082413096045391915/1323284831550836838). **Please note that without a log file, we won't be able to review your suggestion**.

## List of airports with custom operations

::spantable::
| Continent @span | | Country | Airports |
|-----------|-|---------|-----------|
| North America @span | |  |  |
| | | Canada | CYEG, CYHZ, CYOW, CYUL, CYVR, CYWG, CYYC, CYYZ |
| | | USA | KABQ, KAFW, KASE, KATL, KAUS, KAVL, KBDL, KBFI, KBFL, KBNA, KBOI, KBOS, KBUF, KBUR, KBWI, KCID, KCLE, KCLT, KCMA, KCNO, KCRP, KCRQ, KCVG, KDAB, KDAL, KDCA, KDEN, KDFW, KDTW, KEGE, KELP, KEUG, KEWR, KFAR, KFAT, KFLL, KGEG, KGFK, KGJT, KGSP, KHOU, KHPN, KIAD, KIAH, KILM, KIND, KJAN, KJAX, KJFK, KLAS, KLAX, KLGA, KLGB, KMCI, KMCO, KMDT, KMDW, KMEM, KMIA, KMKE, KMSP, KMSY, KMYR, KOAK, KOKC, KOMA, KONT, KORD, KORF, KPAE, KPBI, KPDX, KPHL, KPHX, KPIT, KPVD, KRDU, KRIC, KRNO, KRNT, KROC, KRSW, KSAN, KSAT, KSAV, KSBA, KSBP, KSDF, KSEA, KSFO, KSGF, KSJC, KSLC, KSMF, KSMX, KSNA, KSTL, KSUX, KSYR, KTCM, KTEB, KTIW, KTLH, KTPA, KTUS, KVNY |
| | | Mexico | MDPC, MDPP, MDSD, MHLM, MHTG, MMGL, MMMX, MMMY, MMPR, MMSM, MMTJ, MMUN, MNMG, MPTO, MRLB, MROC, MYNN |
| Africa @span | |  |  |
| | | Algeria | DAAG |
| | | Tunisia | DTTA |
| | | South Africa | FACT, FAOR |
| | | Madagascar | FMEE |
| | | Ethiopia | HAAB |
| | | Egypt | HECA |
| | | Kenya | HKJK, HKMO |
| Europe @span | |  |  |
| | | Belgium | EBBR, EBCI, EBLG |
| | | Germany | EDDB, EDDF, EDDG, EDDH, EDDK, EDDL, EDDM, EDDS, EDDV, EDXW |
| | | UK | EGAA, EGAC, EGBB, EGCC, EGGD, EGGP, EGGW, EGHI, EGJB, EGJJ, EGKK, EGLL, EGNT, EGNX, EGPF, EGPH, EGPK, EGSS, EGTE |
| | | Netherlands | EHAM, EHGG |
| | | Ireland | EICK, EIDW, EINN |
| | | Denmark | EKCH, EKYT |
| | | Latvia | EVRA |
| | | Spain | LEAL, LEBB, LEBL, LEBZ, LEGR, LEMD, LEMG, LEPA, LERS, LESO, LEST, LESU, LEVC, LEVT, LEZG, LEZL |
| | | France | LFBD, LFBE, LFBO, LFBZ, LFCK, LFKC, LFKJ, LFLC, LFLL, LFLS, LFML, LFMN, LFMP, LFMT, LFPB, LFPG, LFPO, LFQQ, LFRN, LFRS, LFSB, LFST, LFTW |
| | | Greece | LGAV, LGIR, LGKL, LGKO, LGKR, LGKV, LGMK, LGPZ, LGRP, LGSA, LGSM, LGSR, LGTS, LGZA |
| | | Hungary | LHBP |
| | | Italy | LIBD, LIBP, LIBR, LICB, LICJ, LICT, LIMC, LIME, LIMF, LIMJ, LIML, LIMP, LIMZ, LIPE, LIPH, LIPR, LIPX, LIPY, LIPZ, LIRA, LIRF, LIRI, LIRN, LIRP, LIRQ, LIRZ |
| | | Czech Republic | LKPR |
| | | Malta | LMML |
| | | Portugal | LPPR, LPPT |
| | | Switzerland | LSGG, LSGS, LSZA, LSZB, LSZH |
| | | Turkey | LTAC, LTAI, LTAU, LTBJ, LTBS, LTCC, LTCG, LTCI, LTFE, LTFG, LTFH, LTFJ, LTFM |
| Oceania @span | |  |  |
| | | Fiji | NFFN |
| | | New Zealand | NSFA, NSTU |
| | | Australia | YMEN, YMML |
| Asia @span | |  |  |
| | | Bahrain | OBBI |
| | | Saudi Arabia | OEJN, OERK |
| | | Iran | OIIE |
| | | Kuwait | OKKK |
| | | Lebanon | OLBA |
| | | UAE | OMAA, OMDB, OMSJ |
| | | Pakistan | OPIS |
| | | Taiwan | RCSS, RCTP |
| | | Japan | RJAA, RJBB, RJCC, RJCH, RJCO, RJFF, RJFK, RJFM, RJFO, RJFT, RJFU, RJGG, RJNK, RJOA, RJOB, RJOH, RJOO, RJOS, RJOT, RJSN, RJSS, RJTT |
| | | South Korea | RKJJ, RKPC, RKPK, RKSI, RKSS, RKTN, RKTU |
| | | Philippines | RPLL |
| | | Nepal | VNKT, VNLK, VNPL |
| | | India | VOBL, VOHS, VOMM, VOVZ |
| | | Thailand | VTBD, VTBS, VTSP |
| | | Vietnam | VVDN, VVNB, VVTS |
| | | Indonesia | WIDD, WIHH, WIII, WIMM |
| | | Malaysia | WMKK, WMKL |
| | | China | ZSOF, ZSPD |
| South America @span | |  |  |
| | | Argentina | SAAR, SACO, SAEZ, SASA, SASJ, SAWH |
| | | Brazil | SBAR, SBBE, SBBI, SBBR, SBCF, SBCG, SBCT, SBCY, SBEG, SBFI, SBFL, SBFZ, SBGL, SBGO, SBGR, SBJP, SBJR, SBJV, SBKP, SBMN, SBMO, SBNF, SBNT, SBPA, SBPS, SBPV, SBRF, SBRJ, SBRP, SBSG, SBSP, SBSV, SBTE, SBVT |
| | | Chile | SCCI, SCEL, SCFA, SCIE |
| | | Ecuador | SEGU, SEQM |
| | | Colombia | SKBO, SKCG, SKMD, SKRG |
| | | Peru | SPJC, SPZO |
::end-spantable::