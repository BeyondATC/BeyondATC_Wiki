---
hide:
  - navigation
  - toc

og_image: https://wiki.beyondatc.net/assets/cards/card-traffic-sliders.png
og_description: Traffic sliders are a setting that manages a queue of data for that particular slider. We pull in data for around 15 hours future and 5 hour past at the airport you are at, and the sliders slice the data from that pool.
description: Traffic sliders are a setting that manages a queue of data for that particular slider. We pull in data for around 15 hours future and 5 hour past at the airport you are at, and the sliders slice the data from that pool.

---

# How the traffic sliders work?

They are a setting that manages **a queue of data** for that particular slider. We pull in data for around 15 hours future and 5 hour past at the airport you are at, and the sliders slice the data from that pool.

**Parked** - it is a slice of data through that time range. The higher the slider, the more parked aircraft there will be. All of these aircraft will be available to depart either because their departure time comes up, or they 'turn around' as the same aircraft by registration is now leaving to somewhere else. We don't inject the aircraft with the same reg more than once. It is reused as required. 

This setting can impact your MSFS framerate the most of the 4 sliders, the best approach is to visit a very busy airport like KLAX, EGLL, EDDF in the peak hour. Set this slider to suit your system at this busy airport. You don't need to touch it again.

**Departures** - this slider is linked to the amount of parked aircraft, in that you can not have more departures than parked aircraft. The slider reflects the size of the departure queue. When an aircraft hits its departure time, it is added to the queue. If there is space based on the density set by the slider, it will depart. If not, it will wait until there is a free slot when another aircraft takes off. So for example on a setting of 1, you should not have more than a couple of aircrafts moving around the airport at a time.

This setting has no impact on MSFS FPS, it is purely to reduce the volume of aircraft moving and on the comms at departure.

**Arrivals** - it is similar to departures but for aircraft on descent or landing phase into the airport. A setting of 1 would again mean only a few arrivals in that phase of flight. In all cases though they are still using arrival times from the real data. It doesn't just mean on a high setting you are going to have arrivals every few seconds. Just more of the scheduled data is active at once.

This setting has minaml impact on MSFS FPS, it is purely to reduce the volume of aircraft moving and on the comms on approach and landing.

**Enroute** - controls how many aircraft you see in the air but that are not flying to or from the airports the player is planned for.

This setting can have an impact on MSFS FPS, as it does increase the overal amount of aircraft Beyond ATC is injecting and managing. Often setting this to the same as parked is a good compromise of performance vs aircraft ammounts.

**A 10 on a slider means no queue** - just use the scheduled time slice of data as is.

A reminder this was never intended as a 'plane spotting' app - we just want decent traffic to fly with!
