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