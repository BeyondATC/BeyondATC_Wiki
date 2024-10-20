---
hide:
  - navigation
  - toc
---

# How the traffic sliders work?

They are a setting that manages **a queue of data** for that particular slider. We pull in data for around 5 hours future and 1 hour past at the airport you are at, and the sliders slice the data from that pool.

**Parked** - it is a slice of data through that time range. The higher the slider, the larger and further out the slice goes. All of these aircraft will be available to depart either because their departure time comes up, or they 'turn around' as the same aircraft by registration is now leaving to somewhere else. We don't inject the aircraft with the same reg more than once. It is reused as required. (if you have evidence in a recent build of duplicate registrations please log it as a bug in the forum)

**Departures** - this slider is linked to the amount of parked aircraft, in that you can not have more departures than parked aircraft. The slider reflects the size of the departure queue. When an aircraft hits its departure time, it is added to the queue. If there is space based on the density set by the slider, it will depart. If not, it will wait until there is a free slot when another aircraft takes off. So for example on a setting of 1, you should not have more than a couple of aircrafts moving around the airport at a time.

**Arrivals** - it is similar to departures but for aircraft on descent or landing phase into the airport. A setting of 1 would again mean only a few arrivals in that phase of flight. In all cases though they are still using arrival times from the real data. It doesn't just mean on a high setting you are going to have arrivals every few seconds. Just more of the scheduled data is active at once.

**Enroute** - similar to parked but taking a slice of data through aircraft in the air but not flying to or from the airports the player is planned for.

**A 10 on a slider means no queue** - just use the scheduled time slice of data as is.

A reminder this was never intended as a 'plane spotting' app - we just want decent traffic to fly with!
