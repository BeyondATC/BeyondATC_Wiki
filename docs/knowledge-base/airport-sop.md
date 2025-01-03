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
| Africa @span | | Algeria | DAAG |
| | | Ethiopia | HAAB |
| | | Egypt | HECA |
| | | Kenya | HKJK, HKMO |
| | | South Africa | FACT, FAOR |
| | | Tunisia | DTTA |
| Asia @span | | Bahrain | OBBI |
| | | China | ZBAA, ZBAD, ZGGG, ZJSY, ZSOF, ZSPD, ZUCK, ZUUU |
| | | Hong Kong | VHHH |
| | | India | VABB, VIDP, VOBL, VOHS, VOMM, VOVZ |
| | | Indonesia | WADD, WIII, WIMM, WIDD |
| | | Iran | OIIE |
| | | Japan | RJAA, RJBB, RJCC, RJCH, RJCO, RJFF, RJFO, RJFM, RJFK, RJFT, RJFU, RJGG, RJNK, RJOA, RJOB, RJOH, RJOO, RJOS, RJOT, RJSS, RJSN, RJTT |
| | | Kuwait | OKKK |
| | | Lebanon | OLBA |
| | | Malaysia | WMKK, WMKL |
| | | Nepal | VNLK, VNPL |
| | | Oman | OOMS |
| | | Pakistan | OPIS |
| | | Philippines | RPLL |
| | | Saudi Arabia | OEJN, OERK |
| | | Singapore | WSSS |
| | | South Korea | RKPC, RKTN, RKTU, RKJJ, RKPK, RKSI, RKSS |
| | | Sri Lanka | VCBI |
| | | Taiwan | RCSS, RCTP |
| | | Thailand | VTBD, VTBS, VTSP |
| | | UAE | OMDB, OMAA, OMSJ |
| | | Vietnam | VVDN, VVNB, VVTS |
| Europe @span | | Austria | LOWG, LOWS, LOWW |
| | | Belgium | EBBR, EBCI, EBLG |
| | | Bulgaria | LBSF, LBBG |
| | | Croatia | LDDU, LDOS, LDPL, LDRI, LDSP, LDZA, LDZD |
| | | Cyprus | LCPH, LCLK |
| | | Czech Republic | LKPR |
| | | Denmark | EKCH, EKYT |
| | | Estonia | EETN |
| | | Finland | EFHK, EFKT, EFIV, EFRO |
| | | France | LFBD, LFBE, LFBO, LFBZ, LFCK, LFKC, LFKJ, LFLC, LFLL, LFLS, LFML, LFMN, LFMP, LFMT, LFMU, LFPB, LFPG, LFPO, LFQQ, LFRN, LFRS, LFSB, LFST, LFTW |
| | | Germany | EDDB, EDDF, EDDG, EDDH, EDDK, EDDL, EDDM, EDDS, EDDV, EDXW |
| | | Greece | LGAV, LGIR, LGKL, LGKO, LGRP, LGKR, LGKV, LGMK, LGPZ, LGSA, LGSM, LGSR, LGTS, LGZA |
| | | Hungary | LHBP |
| | | Ireland | EICK, EIDW, EINN |
| | | Italy | LIBD, LIBP, LIBR, LICB, LICJ, LICT, LIMC, LIME, LIMF, LIMJ, LIML, LIMP, LIMZ, LIPE, LIPH, LIPR, LIPX, LIPY, LIPZ, LIRA, LIRF, LIRI, LIRN, LIRP, LIRQ, LIRZ |
| | | Latvia | EVRA |
| | | Luxembourg | ELLX |
| | | Malta | LMML |
| | | Moldova | LUKK |
| | | Netherlands | EHAM, EHGG |
| | | Norway | ENAL, ENBO, ENBR, ENCN, ENEV, ENGM, ENHD, ENKB, ENTO, ENVA, ENZV |
| | | Poland | EPGD, EPKK, EPKT, EPMO, EPPO, EPWA, EPWR |
| | | Portugal | LPPT, LPPR |
| | | Romania | LRCL, LROP, LRSB, LRTM |
| | | Russia | ULLI, URSS, UUDD, UUEE, UUWW |
| | | Serbia | LYBE |
| | | Slovakia | LZIB, LZKZ |
| | | Slovenia | LJLJ |
| | | Spain | LEAL, LEBB, LEBL, LEBZ, LEGR, LEMD, LEMG, LEPA, LERS, LESO, LEST, LESU, LEVC, LEVT, LEZG, LEZL |
| | | Sweden | ESGG, ESSA, ESSB |
| | | Switzerland | LSGG, LSGS, LSZA, LSZB, LSZH |
| | | Turkey | LTAC, LTAI, LTAU, LTBJ, LTBS, LTCC, LTCG, LTCI, LTFE, LTFG, LTFH, LTFJ, LTFM |
| | | UK | EGAA, EGAC, EGBB, EGCC, EGGD, EGGP, EGGW, EGHI, EGJB, EGJJ, EGKK, EGLL, EGNT, EGNX, EGPF, EGPH, EGPK, EGSS, EGTE |
| North America @span | | Canada | CYEG, CYHZ, CYOW, CYUL, CYVR, CYWG, CYYC, CYYZ |
| | | Dominican Republic | MDPC, MDPP, MDSD |
| | | Honduras | MHLM, MHTG |
| | | Mexico | MMGL, MMMX, MMMY, MMPR, MMSM, MMTJ, MMUN |
| | | Nicaragua | MNMG |
| | | Panama | MPTO |
| | | USA | KABQ, KAFW, KASE, KATL, KAUS, KAVL, KBDL, KBFI, KBFL, KBNA, KBOI, KBOS, KBUF, KBUR, KBWI, KCID, KCLE, KCLT, KCMA, KCNO, KCRP, KCRQ, KCVG, KDAB, KDAL, KDEN, KDCA, KDFW, KDTW, KEGE, KELP, KEUG, KEWR, KFAR, KFAT, KFLL, KGEG, KGFK, KGJT, KGSP, KHOU, KHPN, KIAD, KIAH, KILM, KIND, KJAN, KJAX, KJFK, KLAS, KLAX, KLGA, KLGB, KMCO, KMDW, KMEM, KMIA, KMCI, KMDT, KMKE, KMOT, KMSP, KMSY, KMYR, KOKC, KOAK, KOMA, KONT, KORD, KORF, KPAE, KPBI, KPDX, KPHL, KPHX, KPIT, KPVD, KRDU, KRIC, KRNO, KRNT, KROC, KRSW, KSAN, KSAT, KSAV, KSBA, KSBP, KSDF, KSEA, KSFO, KSGF, KSJC, KSMF, KSLC, KSMX, KSNA, KSTL, KSUX, KSYR, KTCM, KTEB, KTIW, KTLH, KTUS, KVNY, PAJN, PAFA, PANC |
| Oceania @span | | Australia | YBBN, YBCG, YBCS, YBMK, YMEN, YMML, YPAD, YPDN, YPJT, YPPH, YSBK, YSCB, YSSY |
| | | Fiji | NFFN |
| | | French Polynesia | NSFA |
| | | Hawaii | PHNL, PHOG, PHTO |
| | | New Caledonia | NWWW |
| | | New Zealand | NZAA, NZCH, NZHN, NZQN, NZWN |
| South America @span | | Argentina | SAAR, SACO, SAEZ, SASA, SASJ, SAWH |
| | | Brazil | SBAR, SBBE, SBBI, SBBR, SBCF, SBCG, SBCT, SBCY, SBEG, SBFI, SBFL, SBFZ, SBGL, SBGO, SBGR, SBJP, SBJR, SBJV, SBKP, SBNF, SBMN, SBMO, SBNT, SBPA, SBPS, SBPV, SBRF, SBRJ, SBRP, SBSG, SBSP, SBSV, SBTE, SBVT |
| | | Chile | SCCI, SCEL, SCFA, SCIE |
| | | Colombia | SKBO, SKCG, SKMD, SKRG |
| | | Ecuador | SEGU, SEQM |
| | | Peru | SPJC, SPZO |
| | | Uruguay | SUMU |
| | | Venezuela | SVMI |
::end-spantable::
